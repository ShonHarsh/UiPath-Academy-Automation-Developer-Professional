# UiPath - Automation Developer Professional

#### Learning Plan: Automation Developer Professional Training

#### URL: https://academy.uipath.com/learning-plans/automation-developer-professional-training

#### Outline

```
S01P00 State Machines in Studio
  S01P01 Workflow Design-Overview
  S01P02 Understanding State Machines
  S01P03 Build Process with State Machines
  S01P04 Practice - Creating a Vending Machine
  S01P05 State Machine Best Practices
  S01P06 Check your knowledge
  S01P07 Learning Resources
S02P00 Introduction to Robotic Enterprise Framework
  S02P01 Recap: Transactions and types of processes
  S02P02 The dispatcher and performer (producer and consumer) model
  S02P03 Introducing the REFramework template
  S02P04 Overview of the automation project and the main workflow
  S02P05 The Initialization state and the Configuration file
  S02P06 The Get Transaction Data state
  S02P07 The Process Transaction and End Process states
  S02P08 Execution and logging
  S02P09 System and business exception handling
  S02P10 Concurrent queue consumption
  S02P11 Check your knowledge
  S02P12 Learning resources
S03P00 Building a REFramework Project with Orchestrator Queues
S04P00 Building a REFramework Project with Tabular Data
S05P00 Practice with REFramework
S06P00 Orchestrator Triggers and Monitoring
S07P00 Advanced Data Manipulation with Studio
S08P00 Advanced UI Automation with Studio
S09P00 AI Computer Vision with Studio
S10P00 Remote Debugging with Studio
S11P00 Invoke Method and Invoke Code in Studio
S12P00 Automation Developer Professional - Assessment
```

## S01P00 State Machines In Studio

###### S01P01 Workflow Design-Overview

- Flowchart - Allows for visual representation and decision-making in complex scenarios.
- Sequence - A layout for simpler linear flows.
- State Machines - A layout for managing states and transitions.

Question 01/02 Layout that represent multiple branching logical operators, that enable you to create complex business processes and connect activities in multiple ways.

1. Sequence
2. Flowchart [Correct]
3. State Machine
4. Workflow

Question 02/02 The layout in UiPath Studio that enables a more compact representation of logic and is suitable for standard high-level process diagrams of transactional business process templates is:

1. Sequence
2. State Machine [Correct]
3. Flowchart
4. Workflow

###### S01P02 Understanding State Machines

- The Entry section contains the activities that are to be performed when the state is entered.
- The Exit section contains the activities that are to be performed upon exiting the state.
- The Transition sections lets you add activities that will be performed before switching from the current state to the desired state.
- Transitions are created when you link a State to another State or to a Final State, within a State Machine container.
- You can only create one initial state, yet it is possible to have more than one Final State. All state machines must contain an initial state and at least one final state.

```
UiPath Project: S01P02-State-Machine-Air-Conditioning-Representation
```

Question 01/01 The _ _ _ _ _ _ _ _ _ _ _ section lets you add activities that will be performed at entry and exit.

1. Entry
2. Exit
3. Transition [Correct]
4. Final

###### S01P03 Build Process with State Machines

```
UiPath Project: S01P03-State-Machine-AutomatedPayment
```

- It is recommended to define transitions so that only one transition at a time is true.
  -Naming the states in a State Machine is very important for maintenance and future development.
  -In UiPath Studio, the order of the Transitions shown in each State is very important, as it matches the order in which they are evaluated.
- If there are more than one transition defined that can be true, only the first one defined will be executed.

Question01/01 What is the primary function of the Entry and Exit sections in a process or system?

1. They display all the transitions linked to the selected state.
2. They allow you to add entry and exit triggers for the selected state.
3. They provide a clear view of how states are connected to each other.
4. They define the sequence of activities in a process. [Correct]

###### S01P04 Practice - Creating a Vending Machine

```
UiPath Project: S01P04-State-Machine-VendingMachine
```

###### S01P05 State Machine Best Practices

Incorporate the following best practices while working with State Machines:

- Use State Machines for Complex Workflows: State Machines are ideal for managing complex workflows with multiple states, decision points, and conditional transitions. Utilize them when you need to handle intricate business processes that involve various steps and stages.
- Use Transitions Wisely: Utilize transitions to move between states based on specific conditions. Keep transitions simple and easy to understand. Avoid overly complex transition conditions that may cause confusion.
- Error Handling and Recovery: Incorporate error handling mechanisms within states or as a separate state for robust automation. Implement "Try-Catch" blocks to catch exceptions and handle failures gracefully. Plan for potential errors and create appropriate error recovery strategies.
- Clear Naming Conventions: Use descriptive and meaningful names for states and transitions to enhance the readability of your State Machine. This helps other team members understand the workflow easily.
- Logging and Debugging: Implement logging and debugging mechanisms to track the progress of your State Machine. Proper logging will assist in identifying issues and monitoring the automation's performance.
- Testing and Validation: Thoroughly test your State Machine with various scenarios to ensure that it behaves as expected. Validate its performance, handling of different conditions, and response to exceptions.
- Documentation: Provide clear documentation for your State Machine, explaining its purpose, states, transitions, and usage guidelines. Proper documentation helps with knowledge transfer and maintenance.

###### S01P06 Check your knowledge

Question 01/08 Review Question : To improve readability, variable and argument names must align to a naming convention. If a variable is written as FirstName, then what is the naming convention followed?

1. Kebab case
2. Pascal case [Correct]
3. Lower camel case
4. Snake case

Question 02/08 Which of these statements are true regarding simple and final states?

1. The State activity contains three sections, Entry, Exit, and Transition(s), while the Final State contains only one section, Entry. [Correct]
2. The Final State is a State Machine specific activity that ends a State Machine cycle. [Correct]
3. While in a process there can be only one Initial State, multiple Final States can be added. [Correct]
4. The Final State is a State Machine specific activity that ends e Final States can be added. [Correct]
5. The Final State is a State Machine specific activity that ends a State Machine cycle, while the State activity can be used in other workflows as well.

Question 03/08 What is the process for moving from one state to another in a State Machine?

1. Using the "GoToState" activity.
2. Using the "Transition" activity. [Correct]
3. Using the "NextState" activity.
4. Using the "Continue" activity.

Question 04/08 What is a Trigger?

1. An activity that causes a transition to occur. [Correct]
2. An activity that is executed when performing a certain transition.
3. An activity executed when entering the state.
4. An activity that represents the completion of the State Machine.

Question 05/08 Review Question : Which activity can be used to process every item in a collection individually?

1. While
2. If
3. Do While
4. For Each [Correct]

Question 06/08 Which of these statements is true?

1. A state machine workflow can have multiple initial states depending on the set conditions in the transitions, and at least one final state.</br>
   Each state that is not a final state must have at least one transition.
2. A state machine workflow must have one and only one initial state, the Final State is not required.</br>
   Each state must have at least one transition.
3. A state machine workflow must have one and only one initial state, and at least one final state.</br>
   Each state that is not a final state must have at least one transition. [Correct]
4. A state machine workflow must have one and only one initial state, and at least one final state.</br>
   The final state must have at least one transition.

Question 07/08 What is the main difference between a Flowchart layout and a State Machine layout?

1. The Flowchart layout uses a network of linked States to create arbitrary loops or to divert the flow of execution to anywhere else in the workflow at any given time.
   The State Machine workflow can go into a state when it is triggered by an activity.
2. The Flowchart layout uses a network of linked Nodes to create arbitrary loops or to divert the flow of execution to another State in the workflow at any given time.
   The State Machine workflow uses a finite number of States in its execution.
3. The Flowchart layout is used for linear processes as they enable the transition from one activity to another seamlessly, and act as a single block activity.
   State Machines use states and transitions to model workflows in an event-driven manner.
4. Flowcharts present multiple branching logical operators, that enable you to create complex business processes and connect activities in multiple ways.
   State Machines use states and transitions to model workflows in an event-driven manner. [Correct]

Question 08/08 What is a Self-Transition?

1. A state that doesn't need a transition to move into the next state.
2. A transition that moves into the next State based on a trigger.
3. A transition that has no trigger set and is dependent just on the set condition.
4. A transition that moves from a State to itself. [Correct]

###### S01P07 Learning Resources

- UiPath Documentation - [State Machines](https://docs.uipath.com/studio/standalone/2022.10/user-guide/state-machines)
- UiPath Documentation - [Workflow Design](https://docs.uipath.com/studio/standalone/2022.10/user-guide/workflow-design)
- UiPath Documentation - [Project Organization](https://docs.uipath.com/studio/standalone/2022.10/user-guide/project-organization)
- Microsoft.NET Documentation - [State Machine Workflows](https://learn.microsoft.com/en-us/dotnet/framework/windows-workflow-foundation/state-machine-workflows#state-machine-terminology)

## S02P00 Introduction to Robotic Enterprise Framework

###### S02P01 Recap: Transactions and types of processes

Types of business processes
- **Linear** - Steps are run once on a single data set
- **Iterative** - Steps are performed multiple times, each on different data
- **Transactional** - Steps are performed multiple times on different data but the automation design is such that each repeatable part processes independently.

What is a transaction? A transaction represents the minimum (atomic) amount of data and the necessary steps required to process the data, by fulfilling a section of a business process. A typical example would be a process that reads a single email from a mailbox and extracts data from it.

We call the data atomic because once it is processed, the assumption is that we no longer need it as we advance with the business process.

Question 01/01 Match the description of the process with the right transaction processing model.
1. Linear - Creating an account for a new hire, based on an email.
2. Iterative - Creating accounts for the new hires from an Excel file sent via email.
3. Transactional - Creating accounts for the new hires in a live Excel file, where entries are added hourly.

###### S02P02 The dispatcher and performer (producer and consumer) model

- **The Dispatcher** (Producer) reads rows from the input spreadsheet and adds the data (i.e., name and email) to a queue; each queue item will have both name and email from one spreadsheet row.
- **The Performer** (Consumer) retrieves an item from the same queue and does the necessary actions using that data, like replacing template values and sending an email.

A queue is in between the dispatcher and performer.

- Data Source -> **Dispatcher** -> Multi-threaded queues
- Queues <-> **Performer**

The advantages of the Dispatcher and Performer model using REFramework :
- Better separation of actions (between dispatcher/producer or performer/consumer).
- Better separation and distinction between architecture and process layers.
- Built-in error handling and retry mechanism.
- Possibility to run processes across several machines (availability and scalability).
- Better reusability within the project's created components.
- Improved built-in configuration and Orchestrator integration.
- Automation projects created previously without ReFramework can be easily adapted and deployed using the Dispatcher and Performer model.

Question 01/01 In a standard Dispatcher/Performer implementation, which type of process updates the status of a queue item?
1. Dispatcher
2. Performer [Correct]

###### S02P03 Introducing the REFramework template

**The Robotic Enterprise Framework (REFramework)** is a UiPath Studio template of state machines built to best practices regarding logging, exception handling, application initialization, and being ready to tackle any business scenario. It has containers for initializing applications, retrieving input data, processing the data, and ending the transaction

REFramework States - Initialization, Get Transaction Data, Process Transaction, End Process

- UiPath Documentation - [Robotic Enterprise Framework](https://docs.uipath.com/studio/standalone/2022.10/user-guide/robotic-enterprise-framework)

Question 01/01 Match each state with its corresponding description.
1. Initialization - Read the configuration file and initialize the applications used in the process.
2. Get Transaction Data - Get the next transaction to be processed.
3. Process Transaction - Process a single transaction.
4. End Process - Finalize the process and close all applications used.

###### S02P04 Overview of the automation project and the main workflow

```
UiPath Project: S02P04-REFramework-Introduction
```

Main Takeaways
- The overall organization of the template makes it easier to build upon it and is a good starting point for any process.
- Depending on certain conditions, the execution can transition from one state to another to represent the steps of a process.
- Several benefits of using the template stand out: a consistent model which enables development standards, better visibility of actions and events, and ease of the development effort.

```
File Resource: S02P04-REFramework Documentation-EN-2022.10.pdf
```

Question 01/01 If no data is found during the execution of the Get Transaction Data state, what state does the process transition to next?
Initialization
Process Transaction
End Process [Correct]
Get Transaction Data

###### S02P05 The Initialization state and the Configuration file



###### S02P06 The Get Transaction Data state



###### S02P07 The Process Transaction and End Process states



###### S02P08 Execution and logging



###### S02P09 System and business exception handling



###### S02P10 Concurrent queue consumption



###### S02P11 Check your knowledge



###### S02P12 Learning resources


----

----

----

----

----

----

----

----

----

----




Question 01/15 In the Initialization state, all the necessary applications have been initialized and the settings required for the process have been read. Which transition is executed next?

1. Transition: System Exception<br />
   Next state: End Process
2. Transition: No Data<br />
   Next state: End Proces
3. Transition: Successful<br />
   Next state: Get Transaction Data  [Correct]
4. Transition: New Transaction<br />
   Next state: Process Transaction

Question 02/15 A Consumer process gets queue items and enters the data in the UI Demo app. The application has stopped responding while processing an item. Which transition is executed next?

1. Transition: New Transaction<br />
   Next state: Process Transaction
2. Transition: Business Exception<br />
   Next state: Get Transaction Data
3. Transition: Success<br />
   Next state: Get Transaction Data
4. Transition: System Exception<br />
   Next state: Initialization [Correct]

Question 03/15 The automation tries to retrieve a new transaction item in the Get Transaction Data State, but all the transaction items have been already processed. Which transition will execute next?

1. Transition: System Exception<br />
   Next state: End Process
2. Transition: No Data<br />
   Next state: End Process [Correct]
3. Transition: New Transaction<br />
   Next state: Process Transaction
4. Transition: Successful<br />
   Next state: Get Transaction Data

Question 04/15 In which state is the TransactionItem object assigned to the variable?

1. Process Transaction
2. End Process
3. Get Transaction Data [Correct]
4. Initialization

Question 05/15 What is the purpose of the ConsecutiveSystemExceptions variable?

1. Used during transitions between states to represent exceptions other than business exceptions.
2. Used to control the number of consecutive system exceptions. [Correct]
3. Used to control the number of consecutive business exceptions.
4. Used to control the number of attempts of retrying the transaction processing in case of system exceptions.

Question 06/15 Out of the box, what are the workflows that are invoked in the End Process state in a REFramework project?

1. Choose two of the options below.
2. TakeScreenshot
3. CloseAllAplications [Correct]
4. KillAllProcesses [Correct]
5. RetryCurrentTransaction

Question 07/15 What is the Variable Type for the Config variable?

1. DataTable
2. String
3. QueueItem
4. Dictionary [Correct]

Question 08/15 You want to mark a Job as Faulted in Orchestrator, for any error during the Initialization state. You'll assign the TRUE or FALSE value to the  ShouldMarkJobAsFaulted constant, in the Config file?

1. False
2. True [Correct]

Question 09/15 Out of the box, what are the workflows that are invoked in the Initialization state in a REFramework project?
Choose three of the options below.

1. InitAllSettings [Correct]
2. KillAllProcesses [Correct]
3. InitAllApplications [Correct]
4. TakeScreenshot
5. Process
6. SetTransactionStatus

Question 10/15 In which state is the screen resolution logged?

1. Get Transaction Data
2. Process
3. Initialization [True]
4. End Process

Question 11/15 An automation processes emails. A check done in the Process state determines that the numeric values from an email exceed the set threshold, in the Config file, for the processing. Which transition will execute next?

1. Transition: System Exception<br />
   Next state: End Process
2. Transition: New Transaction<br />
   Next state: Process Transaction
3. Transition: Successful<br />
   Next state: Get Transaction Data [Correct]
4. Transition: No Data<br />
   Next state: End Proces

Question 12/15 The TransactionNumber is modified in which workflows?

1. SetTransactionStatus [Correct]
2. GetTransactionData
3. Process
4. InitAllSettings
5. RetryCurrentTransaction [Correct]

Question 13/15 Out of the box, what are the workflows that are invoked in the Process Transaction state in a REFramework project?

1. InitAllSettings
2. GetTransactionData
3. InitAllApplications
4. Process [Correct]
5. RetryCurrentTransaction [Correct]
6. SetTransactionStatus [Correct]

Question 14/15 What statements best describes the functionality of the GetTransactionData workflow?  

1. Retrieves data only from an Excel file.
2. Retrieves data from any defined source (queues, Excel files, file paths). [Correct]
3. Retrieves data only from file paths.
4. Retrieves data only from an Orchestrator Queue.

Question 15/15 In which sheet of the Config file will you define a credential asset?

1. Constants
2. Assets
3. Settings [Correct]

## S03P00 Building a REFramework Project with Orchestrator Queues

Question 01/10 What activity does the REFramework use to update a transaction's status when an Orchestrator queue is the transaction data source?

1. Set Transaction Progress
2. Wait Queue Item
3. Set Transaction Status [Correct]
4. Postpone Transaction Item

Question 02/10 Match the process workflows with the project files where they are invoked.

1. Is invoked in the 'CloseAllApplications' file. [Application1_Close.xaml]
2. Is invoked in the 'Process' file. [Application1_AddTransaction.xaml]
3. Is invoked in the 'KillAllProcesses' file [Application1_ForceClose.xaml]
4. Is invoked in the 'InitAllApplications' file. [Application1_OpenAndLogin.xaml]

Question 03/10 What constant must be configured to increase the number of times the automation retries to get a transaction item?

1. RetryNumberSetTransactionStatus
2. MaxRetryNumber
3. LogMessage_GetTransactionData
4. RetryNumberGetTransactionItem [Correrct]

Question 04/10 Which Config parameter allows developers to set a maximum number for allowed consecutive system exceptions?

1. Postpone Transaction Item
2. MaxConsecutiveSystemException [Correct]
3. MaxRetryNumber
4. Wait Queue Item

Question 05/10 The 'Max number of retries' for a Queue is set to 1. At runtime, the automation processing the queue encounters a Business Rule Exception for one of the transactions. What happens next?

1. The automation retries the transaction once, right away even if there are other transactions in the queue with the same priority.
2. The automation execution terminates because of the Business Rule Exception.
3. The automation retries the transaction until it is successfully processed.
4. The automation does not retry the faulty transaction and continues with the remaining ones. [Correct]

Question 06/10 Review Question: What is the purpose of the ConsecutiveSystemExceptions variable? [Correct]

1. Used to control the number of consecutive system exceptions.
2. Used during transitions between states to represent exceptions other than business exceptions.
3. Used to control the number of attempts of retrying the transaction processing in case of system exceptions.
4. Used to control the number of consecutive business exceptions.

Question 07/10 A developer plans to run a process on different machines that hold different target application paths. How can they manage this?

1. Create an application path Asset with different values per Robot in Orchestrator and reference it in the Assets sheet in the Config file. [Correct]
2. Create a separate entry for each machine in the Settings sheet of the Config file and configure the process to pick one depending on which machine it runs on.
3. Under these conditions, they cannot run the process on different machines. All machines running the process must hold the same target application path.
4. Specify one application path in the Configuration file and manually update the 'Settings' sheet whenever the machine changes.

Question 08/10 What is the queue item processing order criterion when there are no deadline dates specified, and all the transactions have the same priority?

1. First In, First Out [Correct]
2. Last In, First Out
3. First In, Last Out
4. Random Order

Question 09/10 Review Question: Which statements best matches the functionality of the GetTransactionData workflow?  

1. Retrieves data only from file paths.
2. Retrieves data only from an Excel file.
3. Retrieves data only from an Orchestrator Queue.
4. Retrieves data from any defined source (queues, Excel files, file paths). [Correct]

Question 10/10 In what sheet of the config file would a developer set the Max Retry Number?

1. Constants [Correct]
2. Settings
3. Assets
4. Variables

## S04P00 Building a REFramework Project With Tabular Data

Question 01/10 When building a REFramework project, is it possible to use both tabular data for the TransactionItem and Orchestrator assets?

1. No. Orchestrator Assets can only be used when QueueItems are used.
2. Yes. Assets can be used independently from Queues. [Correct]

Question 02/10 In a REFramework project, if the TransactionData is an Array of Strings, what will be the type for TransactionItem?

1. String[]
2. Datarow
3. Queueitem
4. String [Correct]

Question 03/10 What action does a developer need to take to enable the MaxConsecutiveSystemExceptions feature in a REFramework project?

1. No action required, it is enabled by default.
2. Set the MaxConsecutiveSystemExceptions constant value to greater than zero [Correct]
3. Set the MaxRetryNumber constant value to greater than zero
4. Set the  MaxConsecutiveSystemExceptions constant value to zero

Question 04/10 In the REFramework template, which argument in the Process workflow should hold the business context information?

1. io_TransactionData
2. in_TransactionItem [Correct]
3. in_TransactionNumber
4. in_Config

Question 05/10 Which workflow in the REFramework template resets the ConsecutiveSystemException counter to zero?

1. CloseAllApplications
2. SetTransactionStatus [Correct]
3. GetTransactionData
4. RetryCurrentTransaction

Question 06/10 What workflow does the When section of the Get Transaction Data test case invoke?

1. SetTransactionStatus.xaml
2. GetTransactionData.xaml [Correct]
3. Process.xaml
4. InitAllSettings workflow

Question 07/10 By default what state does a developer need to configure to adapt the REFramework to a linear process?

1. End Process
2. Process Transaction
3. Initialization
4. Get Transaction Data [Correct]

Question 08/10 By default, what are the three places where the SetTransactionStatus workflow is invoked in a REFramework project?

1. In the 'Try' block of the process transaction state. [Correct]
2. In the 'Finally' block of the Process Transaction state.
3. In the 'System Exception' section in the catch section of process transaction state. [Correct]
4. In the 'Business Rule Exception' section in the catch section of process transaction state. [Correct]

Question 09/10 An error is encountered during the execution of the GetTransactionData state in a REFramework process. The number of retries exceeds the maximum, what state will be executed next?

1. Get Transaction Data
2. Initialization
3. End Process [Correct]
4. Process Transaction

Question 10/10 When building a REFramework project, a developer plans to use tabular data instead of an Orchestrator queue. Which activity do they need to replace in the default REFramework template to retrieve the transaction data?

1. The Get Transaction Item activity in the Get Transaction Data state.
2. The Get Transaction Item activity in the Process Transaction  state. [Correct]
3. The Assign activity in the Get Transaction Data state.
4. The Get Queue Item activity in the Process Transaction state.

## S05P00 Practice with REFramework

## S06P00 Orchestrator Triggers and Monitoring

## S07P00 Advanced Data Manipulation with Studio

## S08P00 Advanced UI Automation with Studio

## S09P00 AI Computer Vision with Studio

## S10P00 Remote Debugging with Studio

## S11P00 Invoke Method and Invoke Code in Studio

## S12P00 Automation Developer Professional - Assessment
