---
UID: NF:mstask.IScheduledWorkItem.GetExitCode
title: IScheduledWorkItem::GetExitCode
author: windows-sdk-content
description: Retrieves the last exit code returned by the executable associated with the work item on its last run. The method also returns the exit code returned to Task Scheduler when it last attempted to run the work item.
old-location: taskschd\ischeduledworkitem_getexitcode.htm
old-project: taskschd
ms.assetid: 857d8b84-2ccf-4888-8aea-869ba70d3f64
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetExitCode, GetExitCode method [Task Scheduler], GetExitCode method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetExitCode method, IScheduledWorkItem.GetExitCode, IScheduledWorkItem::GetExitCode, _msb_ischeduledworkitem_getexitcode, mstask/IScheduledWorkItem::GetExitCode, taskschd.ischeduledworkitem_getexitcode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IScheduledWorkItem.GetExitCode
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IScheduledWorkItem::GetExitCode


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the last exit code returned by the executable associated with the <a href="w.htm">work item</a> on its last run. The method also returns the exit code returned to Task Scheduler when it last attempted to run the work item.


## -parameters




### -param pdwExitCode [out]

A pointer to a <b>DWORD</b> value that is set to the last exit code for the work item. This is the exit code that the work item returned when it last stopped running. If the work item has never been started, 0 is returned.


## -returns



The 
<b>GetExitCode</b> method returns the error from the last attempt to start the work item. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The attempt to start the work item was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_S_TASK_HAS_NOT_RUN</b></dt>
</dl>
</td>
<td width="60%">
No attempt has ever been made to start this work item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available.

</td>
</tr>
</table>
 




## -remarks



This method can  return the following two pieces of information:

<ul>
<li>The error or exit code that is returned by the executable that is being scheduled is returned in the <i>pdwExitCode</i> parameter.</li>
<li>The error code that the Task Scheduler received when it tried to start the job is returned in the 
<b>GetExitCode</b> method call itself.</li>
</ul>
To obtain an updated error code, always call  <a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">ITaskScheduler::Activate</a> first to obtain a new <a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a> interface, which can then be used to obtain the updated error codes.


#### Examples

For an example of how to retrieve the creator of a task, see <a href="https://msdn.microsoft.com/e7bfe645-7f4c-4700-9adf-c581e6895aec">C/C++ Code Example: Retrieving Task Exit Code</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>
 

 

