# ikurtz.github.io

# LAB 1: Configuring High Availability (HA) For Your CloudBees CI Managed Controller

In this exercise, you will complete the following tasks:

- Task 1: Verify that your controller runs in High Availability mode.
- Task 2: Switch to another replica.
- Task 3: Enable developer mode.
- Task 4: Switch back to the original replica.
- Task 5: Review the HA information displayed by the replica when running in developer mode.

## Verify that Your Managed Controller Runs in HA mode
As you are using a modern CloudBees CloudBees CI platform from your operations center’s root level:

- Verify that `controller-2` has two replicas and both are available.
- Navigate to **Controller-2 > Manage Jenkins > High Availability**
- Review the information displayed on the High Availability screen about the number of replicas and the replica you are currently using.

## Switch to Another Replica
- Select the `Reset sticky session` button and reload the **High Availability** screen as many times as needed until you are randomly assigned to the other replica.

## Enable developer mode
- In the **High Availability** screen, check the **Enable developer mode** and select **Apply**.
- Reload the **High Availability Screen** and verify the information displayed.

Sample output

## Switching Back to the Original Replica
- Navigate to the **Manage Jenkins > High Availability** screen.
- Select the `Reset sticky session` button and reload the **High Availability** screen as many times as needed until you are back to the original replica (the second one in our case).

Sample output

## Review the HA Information Displayed by the Replica When Running in Developer Mode
- On `controller-2` navigate to **Team-CD > Job**.
- Run the `Job` Pipeline by selecting **Build Now** on the left navigation pane.
- Verify that the running build adds the name of the replica owning the build to its name.

Example 1. Sample output
