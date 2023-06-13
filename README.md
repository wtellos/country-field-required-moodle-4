# country-field-required-moodle-4

Core-code altering for Moodle 4 registration form to make the Country field required.
Please keep in mind that this is a core file, any changes made will be overwritten during upgrades.

# Steps:
Locate folder  the: /login/signup_form.php

Locate line of code:
$mform->addElement('select', 'country', get_string('country'), $country);

and replace with:
$mform->addElement('select', 'country', get_string('country'), $country, ['required' => true]);

Added below line for enabling the required fa-icon:

$mform->addRule('country', get_string('placeholdertypeorselect'), 'required', null, 'client'); 
