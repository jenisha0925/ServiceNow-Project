IMPLEMENT CLIENT SCRIPT AND UI POLICY IN SERVICENOW

 Introduction

ServiceNow is a cloud-based platform widely used for IT Service Management (ITSM) and workflow automation. It provides various tools to customize forms and enforce business rules. UI Policies and Client Scripts are important features that help improve user experience and ensure data accuracy.

This project demonstrates the implementation of UI Policies and different types of Client Scripts on the Incident table in ServiceNow. The project focuses on controlling field behavior, validating user inputs, and restricting unauthorized actions during incident management.

Objective

The objectives of this project are:

* To create and configure UI Policies on the Incident table.
* To implement UI Policy Actions for field control.
* To create and test OnChange Client Scripts.
* To create and test OnSubmit Client Scripts.
* To create and test OnCellEdit Client Scripts.
* To improve data validation and user interaction.

Tools and Technologies Used

* ServiceNow Platform
* Incident Table
* UI Policies
* UI Policy Actions
* Client Scripts
* Web Browser

Project Description

The project was developed on the Incident table in ServiceNow. The implementation includes a UI Policy and multiple Client Scripts to control form behavior and validate user actions.

UI Policy

A new UI Policy was created on the Incident table with the following condition:

Impact = High

Whenever the impact value is set to High, the policy becomes active and executes the configured actions.

UI Policy Actions

Two UI Policy Actions were configured:

Assignment Group Field

* Mandatory: True
* Read Only: False

This ensures that the Assignment Group field must be filled when the impact is High.

 Urgency Field

* Read Only: True

This prevents users from modifying the Urgency field when the policy condition is met.

Client Script Implementation

 OnChange Client Script

An OnChange Client Script was created on the Incident table. This script executes whenever the selected field value changes and performs the required client-side action.

OnSubmit Client Script

An OnSubmit Client Script was created to validate form submission.

The script checks whether the  Assigned To  field contains a value. If the field is left empty, the system displays a warning message and prevents the form from being submitted.

 OnCellEdit Client Script

An OnCellEdit Client Script was created for the State field.

This script prevents users from modifying the State value directly from the Incident list view and requires them to open the Incident record for updates.

Testing and Results

 UI Policy Testing

An Incident record was opened and the Impact value was changed to High.

Result:
The Urgency field automatically became Read Only, confirming that the UI Policy was functioning correctly.

OnSubmit Client Script Testing

An Incident form was opened and submitted without entering a value in the Assigned To field.

Result:
The system displayed a warning message and blocked the submission. After selecting a user, the form was submitted successfully.

OnCellEdit Client Script Testing

The Incident list view was opened and an attempt was made to change the State field directly from the list.

Result:
The system prevented the update and instructed the user to open the Incident record instead.

 Final Testing

A complete validation was performed by:

1. Setting Impact to High.
2. Verifying mandatory field behavior.
3. Leaving Assigned To empty and attempting submission.
4. Selecting a valid user and submitting the form.

Result:
All UI Policies and Client Scripts worked successfully according to the project requirements.

Advantages

* Improves data accuracy and consistency.
* Reduces user input errors.
* Enhances form validation.
* Enforces organizational business rules.
* Improves overall Incident Management efficiency.

Conclusion

The project successfully implemented UI Policies and Client Scripts on the ServiceNow Incident table. The UI Policy dynamically controlled field behavior based on incident impact, while the OnChange, OnSubmit, and OnCellEdit Client Scripts provided validation and controlled user actions. Testing confirmed that all configurations worked correctly and fulfilled the intended business requirements.

 Future Enhancements

* Implement additional client-side validations.
* Integrate Business Rules and Workflows.
* Add automated notifications.
* Enhance incident automation processes.
