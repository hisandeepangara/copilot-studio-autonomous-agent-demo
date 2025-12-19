# copilot-studio-autonomous-agent-demo

## Problem:
Autonomously determine the claims workflow from a First Notice of Loss (FNOL) document.

## Approach
Below visual flow, describes the approach to solve our problem in an autonmomous agent setup.
<img width="1438" height="497" alt="image" src="https://github.com/user-attachments/assets/e3016a93-af87-4674-936c-b8d2e88a500a" />

1. The agent is triggered when a new FNOL document is received in a monitored inbox.
2. Upon trigger, the agent retrieves the attached FNOL document using the **Get Attachments connector**.
3. The agent then invokes an **AI Builder Prompt** to read and interpret the document, extracting the required key fields and identifying any missing information of interest.
4. Using the extracted data, the agent applies predefined rule-based routing logic, combined with its base response model knowledge, to determine the appropriate claims workflow.
5. Finally, the agent returns a consolidated response containing the extracted fields, identified missing fields, the recommended routing decision, and the reasoning behind that decision.

## Steps to see it in action
1. Download the unmanaged solution from the repository.
2. Navigate to make.powerapps.com and select your target environment.
3. Choose Import solution and upload the downloaded unmanaged solution.
4. Wait for the import to complete, then open the solution and launch the Insurance Claims Processing Agent.
5. Send an email to the mailbox configured during the Outlook connection setup, using **“FNOL”** as the subject and attaching a sample FNOL document.
6. In the agent, open the Overview tab, go to Triggers, and click the Test trigger icon on the “When a new FNOL arrives” trigger.
7. A trigger instance corresponding to step 5 will appear. Select it and click Test.
8. Review the activity map and observe the results in the test pane.

## Video demo:
[Click here to view the video demo]()
