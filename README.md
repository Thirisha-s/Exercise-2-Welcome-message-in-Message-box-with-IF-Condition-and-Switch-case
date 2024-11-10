## Exercise_2-UiPath-Welcome_message_in_Message_box_with_IF_Condition-and-Switch_case
```
Name: THIRISHA S
Reg No: 212222230160
```
## Aim:

To create a UiPath automation process that takes the user's name as input and displays personalized welcome messages based on the input using a IF condition and Switch case activity.

## Equipment Required:

UiPath Studio (installed on a compatible system).
Computer with:
Minimum 4 GB RAM.
Minimum 2.0 GHz CPU.
Windows operating system.
.NET Framework 4.6.1 or later.

## Procedure:
### Start a New Process:

Open UiPath Studio and create a new process.<br>
Name the project UiPath Switch Case Example.<br>

### Add Input Dialog Activity:

In the Activities tab, search for Input Dialog.<br>
Drag and drop the Input Dialog activity onto the main window.<br>
Set the Title property as "Enter Your Name", and the Label as "Please enter your name:".<br>
Create a variable userName to store the input from the user and assign the result to it.<br>

### Add IF Condition:

In the Activities tab, search for the IF.<br>
Drag the IF activity onto the main window, below the Input Dialog activity.<br>
In the Condition field of the IF activity, type userName = "RAM" to check if the user input is "RAM".

### Configure the True Branch:

In the Then section (True branch) of the IF activity, drag a Message Box activity.<br>
Set the Message field to "Welcome Mr. Ramachandran".

### Configure the False Branch:

In the Else section (False branch) of the IF activity, add Switch activity.

### Add Switch Activity:

In the Activities tab, search for the Switch activity.<br>
Drag the Switch activity under the Input Dialog activity.<br>
In the Expression field of the Switch activity, set the value to userName.<br>
Set the TypeArgument to String to handle text-based cases.<br>

### Configure Switch Cases:

Add cases to the Switch activity to handle specific inputs:<br>
a. Case 1: "RAM"<br>

Add a case with the label "RAM".<br>
Drag a Message Box activity into this case.<br>
Set the Message property to "Welcome Mr. Ramachandran".<br>
b. Case 2: "John"<br>

Add a case labeled "John".<br>
Drag a Message Box activity into this case.<br>
Set the Message to "Welcome Mr. John Doe".<br>
c. Case 3: "Sara"<br>

Add a case labeled "Sara".<br>
Drag a Message Box activity into this case.<br>
Set the Message to "Welcome Ms. Sara Smith".<br>

### Configure Default Case:<br>

In the Default section of the Switch, drag a Message Box activity.<br>
Set the Message to "Welcome " + userName, so it displays the user’s name for any other input.<br>

### Save and Run:

Save the project by pressing CTRL+S.<br>
Click on Run from the top-right corner to execute the workflow.

## UiPath WorkFlow:

![Screenshot 2024-09-12 114316](https://github.com/user-attachments/assets/39b63cde-5889-4afa-82fb-2c33b9b4e3e2)
![Screenshot 2024-09-12 114331](https://github.com/user-attachments/assets/d7cab2b7-6fdf-42c9-9fa9-c1f50b236992)
![Screenshot 2024-09-12 114355](https://github.com/user-attachments/assets/7ec2ffa6-8fac-4b1f-aa4b-516ff2fd6c2e)
![Screenshot 2024-09-12 114443](https://github.com/user-attachments/assets/96be57c1-fd34-4656-882a-2a751cb82934)
![Screenshot 2024-09-12 114453](https://github.com/user-attachments/assets/99f35a02-4a8d-4e16-89fb-596ad9d4da03)

## Result:

When the input is "RAM", a message box will display: "Welcome Mr. Ramachandran".<br>
When the input is "John", a message box will display: "Welcome Mr. John Doe".<br>
When the input is "Sara", a message box will display: "Welcome Ms. Sara Smith".<br>
For any other input, the message box will display: "Welcome " followed by the entered name.<br>
This demonstrates how the Switch activity can be used in UiPath to handle multiple cases based on user input.
