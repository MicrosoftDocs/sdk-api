---
UID: NN:mstask.ITask
title: ITask
author: windows-sdk-content
description: Provides the methods for running tasks, getting or setting task information, and terminating tasks. It is derived from the IScheduledWorkItem interface and inherits all the methods of that interface.
old-location: taskschd\itask.htm
old-project: TaskSchd
ms.assetid: 84a70dd0-43cb-42be-8360-35263bf1afb8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ITask, ITask interface [Task Scheduler], ITask interface [Task Scheduler],described, _msb_itask, mstask/ITask, taskschd.itask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mstask.h
req.include-header: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - ITask
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITask interface


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for running tasks, getting or setting task information, and terminating tasks. It is derived from the 
<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a> interface and inherits all the methods of that interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITask</b> interface inherits from <a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>. <b>ITask</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITask</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff8c9c3b-697f-42f0-a5b5-6194e4c89096">CreateTrigger</a>
</td>
<td align="left" width="63%">
Creates a <a href="t.htm">trigger</a> using a work item object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/418e16d3-67ee-4b77-a7a9-67e722619d80">DeleteTrigger</a>
</td>
<td align="left" width="63%">
Deletes a trigger from a work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b0b335a-4386-4726-8758-ef5944cb5dfe">EditWorkItem</a>
</td>
<td align="left" width="63%">
Opens the configuration properties for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5f279ac-bf03-4af5-9bad-58eadaba0ca1">GetAccountInformation</a>
</td>
<td align="left" width="63%">
Retrieves the account name for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79a8c324-1191-412b-be2b-eb5935337925">GetApplicationName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the application that the task is associated with.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49bfd451-8100-40e1-9727-e54c5478b415">GetComment</a>
</td>
<td align="left" width="63%">
Retrieves the comment for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25bbb200-3418-4ca9-87a5-5db537baceee">GetCreator</a>
</td>
<td align="left" width="63%">
Retrieves the creator of the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9935325-124b-4c21-be9c-e9d48fb69791">GetErrorRetryCount</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3ace124-cb02-4d4f-9d6c-18d0d99d64bf">GetErrorRetryInterval</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/857d8b84-2ccf-4888-8aea-869ba70d3f64">GetExitCode</a>
</td>
<td align="left" width="63%">
Retrieves the work item's last exit code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fe3c184-2689-44de-b60f-92d31eaa5285">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves the flags that modify the behavior of the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72d53691-f2ea-4a20-8e85-f9db81f830cd">GetIdleWait</a>
</td>
<td align="left" width="63%">
Retrieves the idle wait time for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9f27929-d304-4696-bb36-0c0a34c71388">GetMaxRunTime</a>
</td>
<td align="left" width="63%">
Retrieves the maximum length of time the task can run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38872c60-7d2b-4bfc-b771-98950ab8f40c">GetMostRecentRunTime</a>
</td>
<td align="left" width="63%">
Retrieves the most recent time the work item began running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a53700f7-0e2c-413f-b7b3-64aa2e970f11">GetNextRunTime</a>
</td>
<td align="left" width="63%">
Retrieves the next time the work item will run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f59118d6-b430-4fcd-9c78-e6b5a65c151a">GetParameters</a>
</td>
<td align="left" width="63%">
Retrieves the command-line parameters of a task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ace8ab8-e629-4cf9-9bdf-416b2f67c4cd">GetPriority</a>
</td>
<td align="left" width="63%">
Retrieves the priority for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fd9f5dc-b237-46a6-96c0-0e4b3accd6e5">GetRunTimes</a>
</td>
<td align="left" width="63%">
Retrieves the work item run times for a specified time period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb0bc52c-ae50-4c14-864d-099f2903adfb">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd919375-c903-45eb-a8f4-45baf5b42203">GetTaskFlags</a>
</td>
<td align="left" width="63%">
Returns the flags used to modify the behavior of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f99b342c-9233-43e3-93f1-88586e975608">GetTrigger</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="t.htm">trigger structure</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db1c98db-c4c1-45af-baba-097ee8dc6abf">GetTriggerCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of triggers associated with a work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e342807-4796-449b-b490-815ce57f4d8f">GetTriggerString</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="t.htm">trigger string</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/737259f6-63d3-43f1-83a7-a10c95aff0e1">GetWorkingDirectory</a>
</td>
<td align="left" width="63%">
Retrieves the working directory of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b37c412-80ed-44fb-8b3a-b142a9669080">GetWorkItemData</a>
</td>
<td align="left" width="63%">
Retrieves application-defined data associated with the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f533fcf6-8ece-442f-b6d5-3702321db9e9">Run</a>
</td>
<td align="left" width="63%">
Runs the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fae1299f-2f3f-48cf-91d9-1057ce62172b">SetAccountInformation</a>
</td>
<td align="left" width="63%">
Sets the account name and password for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bec25a9-e653-48b5-be41-8f513169fc8c">SetApplicationName</a>
</td>
<td align="left" width="63%">
Assigns a specific application to the current task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6017aa1-8860-454c-a402-becbc1a4ee5c">SetComment</a>
</td>
<td align="left" width="63%">
Sets the comment for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e15c6aba-79f7-407f-81d1-b7ec404c68f9">SetCreator</a>
</td>
<td align="left" width="63%">
Sets the creator of the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2c5bafb-a792-4653-87ab-677daec9b10f">SetErrorRetryCount</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5923d76-50d0-4d1c-9d80-0b7cbd8ee3d7">SetErrorRetryInterval</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/640ba3c7-ed9d-4c4c-82fd-34fc777172c2">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the flags that modify the behavior of the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7ad639a-4094-4621-9add-b89958c0bda4">SetIdleWait</a>
</td>
<td align="left" width="63%">
Sets the <a href="i.htm">idle wait time</a> for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb9012c6-be41-4ec6-bb1a-73bd7896738f">SetMaxRunTime</a>
</td>
<td align="left" width="63%">
Sets the maximum length of time the task can run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/094dcd8f-35aa-4300-b58d-c846bca1c88c">SetParameters</a>
</td>
<td align="left" width="63%">
Sets the command-line parameters for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f72e5fb8-761e-41bd-be64-b886ebc2c1e5">SetPriority</a>
</td>
<td align="left" width="63%">
Sets the priority for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32231145-241a-46ff-9c49-94f5bf7cc532">SetTaskFlags</a>
</td>
<td align="left" width="63%">
Sets the flags that modify the behavior of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df12d899-c254-4bbf-a49f-d89a2fcb0e28">SetWorkingDirectory</a>
</td>
<td align="left" width="63%">
Sets the working directory for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9135b37a-d9f8-4bee-a851-9daca6dc733c">SetWorkItemData</a>
</td>
<td align="left" width="63%">
Stores application-defined data associated with the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ea2144b-4f51-41db-8eaf-50da83967ea5">Terminate</a>
</td>
<td align="left" width="63%">
Ends the execution of the work item.

</td>
</tr>
</table> 


## -remarks



<b>ITask</b> is the primary interface of the <a href="t.htm">task trigger object</a>. To create a task object, call 
<a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">ITaskScheduler::Activate</a> for existing tasks or 
<a href="https://msdn.microsoft.com/1fbd65ae-0b54-4175-bf26-4226b1aabdc1">ITaskScheduler::NewWorkItem</a> for new tasks.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/2131b966-6179-4a80-a3f1-ebb8967a7a90">C/C++ Code Example: Terminating a Task</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">ITaskScheduler::Activate</a>



<a href="https://msdn.microsoft.com/1fbd65ae-0b54-4175-bf26-4226b1aabdc1">ITaskScheduler::NewWorkItem</a>
 

 

