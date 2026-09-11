# Test Scenarios

## 1. Registration

| Scenario ID | Test Scenario                                                        | Type     |
| ----------- | -------------------------------------------------------------------- | -------- |
| TS-REG-001  | Verify that a user can register with valid details.                  | Positive |
| TS-REG-002  | Verify registration with an already registered email address.        | Negative |
| TS-REG-003  | Verify registration with all required fields left blank.             | Negative |
| TS-REG-004  | Verify registration with an invalid email format.                    | Negative |
| TS-REG-005  | Verify registration with an invalid or weak password.                | Negative |
| TS-REG-006  | Verify registration when the password confirmation does not match.   | Negative |
| TS-REG-007  | Verify registration using minimum and maximum allowed input lengths. | Edge     |
| TS-REG-008  | Verify registration with leading/trailing spaces in input fields.    | Edge     |

## 2. Login

| Scenario ID  | Test Scenario                                                      | Type     |
| ------------ | ------------------------------------------------------------------ | -------- |
| TS-LOGIN-001 | Verify that a registered user can log in with valid credentials.   | Positive |
| TS-LOGIN-002 | Verify login with an incorrect password.                           | Negative |
| TS-LOGIN-003 | Verify login with an unregistered email address.                   | Negative |
| TS-LOGIN-004 | Verify login with an incorrect email format.                       | Negative |
| TS-LOGIN-005 | Verify login with blank email and password fields.                 | Negative |
| TS-LOGIN-006 | Verify that the password is masked while entering it.              | Positive |
| TS-LOGIN-007 | Verify login using minimum and maximum allowed input lengths.      | Edge     |
| TS-LOGIN-008 | Verify that the user remains authenticated after successful login. | Positive |

## 3. Create Task

| Scenario ID   | Test Scenario                                                          | Type     |
| ------------- | ---------------------------------------------------------------------- | -------- |
| TS-CREATE-001 | Verify that a logged-in user can create a task with valid information. | Positive |
| TS-CREATE-002 | Verify task creation with required fields left blank.                  | Negative |
| TS-CREATE-003 | Verify task creation with minimum allowed input.                       | Edge     |
| TS-CREATE-004 | Verify task creation with maximum allowed input length.                | Edge     |
| TS-CREATE-005 | Verify task creation using special characters where permitted.         | Edge     |
| TS-CREATE-006 | Verify that the newly created task appears in the task list.           | Positive |
| TS-CREATE-007 | Verify that an unauthenticated user cannot create a task.              | Negative |

## 4. View Task List

| Scenario ID | Test Scenario                                                    | Type     |
| ----------- | ---------------------------------------------------------------- | -------- |
| TS-VIEW-001 | Verify that a logged-in user can view the task list.             | Positive |
| TS-VIEW-002 | Verify that newly created tasks are displayed in the list.       | Positive |
| TS-VIEW-003 | Verify that multiple tasks are displayed correctly.              | Positive |
| TS-VIEW-004 | Verify the task list when no tasks exist.                        | Edge     |
| TS-VIEW-005 | Verify that task information displayed in the list is correct.   | Positive |
| TS-VIEW-006 | Verify that a user cannot view another user's private tasks.     | Negative |
| TS-VIEW-007 | Verify that an unauthenticated user cannot access the task list. | Negative |

## 5. Edit Task

| Scenario ID | Test Scenario                                                             | Type     |
| ----------- | ------------------------------------------------------------------------- | -------- |
| TS-EDIT-001 | Verify that a logged-in user can edit an existing task.                   | Positive |
| TS-EDIT-002 | Verify editing a task with valid updated information.                     | Positive |
| TS-EDIT-003 | Verify editing a task with blank required fields.                         | Negative |
| TS-EDIT-004 | Verify editing a task using maximum allowed input length.                 | Edge     |
| TS-EDIT-005 | Verify that updated task information is displayed correctly after saving. | Positive |
| TS-EDIT-006 | Verify that cancelling an edit does not modify the original task.         | Positive |
| TS-EDIT-007 | Verify that a user cannot edit another user's task.                       | Negative |

## 6. Delete Task

| Scenario ID   | Test Scenario                                                                   | Type     |
| ------------- | ------------------------------------------------------------------------------- | -------- |
| TS-DELETE-001 | Verify that a logged-in user can delete an existing task.                       | Positive |
| TS-DELETE-002 | Verify that a confirmation message is displayed before deletion, if applicable. | Positive |
| TS-DELETE-003 | Verify that cancelling deletion keeps the task unchanged.                       | Positive |
| TS-DELETE-004 | Verify that the deleted task is removed from the task list.                     | Positive |
| TS-DELETE-005 | Verify that a deleted task cannot be accessed through the task list.            | Positive |
| TS-DELETE-006 | Verify that a user cannot delete another user's task.                           | Negative |
| TS-DELETE-007 | Verify deletion when the task no longer exists in the database.                 | Edge     |

## 7. Input Validation

| Scenario ID  | Test Scenario                                               | Type     |
| ------------ | ----------------------------------------------------------- | -------- |
| TS-VALID-001 | Verify validation of mandatory fields.                      | Negative |
| TS-VALID-002 | Verify validation of email format.                          | Negative |
| TS-VALID-003 | Verify validation of password requirements.                 | Negative |
| TS-VALID-004 | Verify minimum input length validation.                     | Edge     |
| TS-VALID-005 | Verify maximum input length validation.                     | Edge     |
| TS-VALID-006 | Verify handling of leading and trailing spaces.             | Edge     |
| TS-VALID-007 | Verify handling of special characters.                      | Edge     |
| TS-VALID-008 | Verify that invalid input does not get submitted or stored. | Negative |

## 8. Error Handling

| Scenario ID  | Test Scenario                                                                           | Type     |
| ------------ | --------------------------------------------------------------------------------------- | -------- |
| TS-ERROR-001 | Verify that an appropriate error message is displayed for invalid login credentials.    | Negative |
| TS-ERROR-002 | Verify that appropriate validation messages are displayed for missing required fields.  | Negative |
| TS-ERROR-003 | Verify that duplicate registration attempts display an appropriate error message.       | Negative |
| TS-ERROR-004 | Verify application behavior when the database is unavailable.                           | Edge     |
| TS-ERROR-005 | Verify application behavior when a server error occurs.                                 | Edge     |
| TS-ERROR-006 | Verify that error messages do not expose sensitive technical information.               | Security |
| TS-ERROR-007 | Verify that the application handles unexpected input without crashing.                  | Edge     |
| TS-ERROR-008 | Verify that users receive an appropriate message when a requested task cannot be found. | Negative |
