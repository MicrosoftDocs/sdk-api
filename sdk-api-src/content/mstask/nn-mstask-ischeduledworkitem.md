---
UID: NN:mstask.IScheduledWorkItem
title: IScheduledWorkItem
author: windows-sdk-content
description: Provides the methods for managing specific work items.
old-location: taskschd\ischeduledworkitem.htm
tech.root: taskschd
ms.assetid: e668833a-094d-4504-90a0-87912a6a53c2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IScheduledWorkItem, IScheduledWorkItem interface [Task Scheduler], IScheduledWorkItem interface [Task Scheduler],described, _msb_ischeduledworkitem, mstask/IScheduledWorkItem, taskschd.ischeduledworkitem
ms.topic: interface
req.header: mstask.h
req.include-header: 
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
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IScheduledWorkItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# IScheduledWorkItem interface


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for managing specific <a href="https://msdn.microsoft.com/en-us/library/Aa384011(v=VS.85).aspx">work items</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScheduledWorkItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IScheduledWorkItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IScheduledWorkItem</b> interface has these methods.
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
Creates a <a href="https://msdn.microsoft.com/en-us/library/Aa382533(v=VS.85).aspx">trigger</a> using a work item object.

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
<a href="https://msdn.microsoft.com/f99b342c-9233-43e3-93f1-88586e975608">GetTrigger</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://msdn.microsoft.com/en-us/library/Aa382533(v=VS.85).aspx">trigger structure</a>.

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
Retrieves a <a href="https://msdn.microsoft.com/en-us/library/Aa382533(v=VS.85).aspx">trigger string</a>.

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
Sets the <a href="https://msdn.microsoft.com/en-us/library/Aa446894(v=VS.85).aspx">idle wait time</a> for the work item.

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



The <b>IScheduledWorkItem</b> interface is the base interface for the 
<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a> interface. All methods provided by 
<b>IScheduledWorkItem</b> are inherited by the 
<b>ITask</b> interface and are typically called through that interface.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/2131b966-6179-4a80-a3f1-ebb8967a7a90">C/C++ Code Example: Terminating a Task</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>
 

 

