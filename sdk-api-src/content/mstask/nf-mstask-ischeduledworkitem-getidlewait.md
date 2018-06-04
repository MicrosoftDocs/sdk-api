---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IScheduledWorkItem::GetIdleWait


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the <a href="i.htm">idle wait time</a> for the work item. 
			
		For information about idle conditions, see <a href="https://msdn.microsoft.com/1e480681-b77a-48fe-a732-dd1591eaa08d">Task Idle Conditions</a>.


## -parameters




### -param pwIdleMinutes [out]

A pointer to a <b>WORD</b> that contains the idle wait time for the current work item, in minutes.


### -param pwDeadlineMinutes [out]

A pointer to a <b>WORD</b> that specifies the maximum number of minutes that the Task Scheduler will wait for the idle-time period returned in <i>pwIdleMinutes</i>.


## -returns



The 
<b>GetIdleWait</b> method returns one of the following values.

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
The operation was successful.

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
</table>
 




## -remarks



The idle time returned here is used in conjunction with <a href="i.htm">idle triggers</a> and <a href="i.htm">idle conditions</a>. Idle triggers are event-based triggers that are not associated with a scheduled time. Idle conditions are associated with the scheduled start time for the task.

Idle triggers are specified by setting the 
<a href="https://msdn.microsoft.com/07cba55c-47af-4879-b7be-12952763e016">TASK_TRIGGER_TYPE</a> member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure to the value TASK_EVENT_TRIGGER_ON_IDLE. The idle trigger is fired when the system becomes idle for the amount of time returned in <i>pwIdleMinutes</i>.

You can set idle conditions by calling 
<a href="https://msdn.microsoft.com/640ba3c7-ed9d-4c4c-82fd-34fc777172c2">IScheduledWorkItem::SetFlags</a>. If the TASK_FLAG_START_ONLY_IF_IDLE flag is set, the work item runs at its scheduled time only if the system becomes idle for the amount of time returned in <i>pwIdleMinutes</i>. The Task Scheduler service will wait up to <i>pwDeadlineMinutes</i> past the scheduled start time to see if the system becomes idle.


#### Examples

For an example of how to retrieve the idle wait time of a task, see <a href="https://msdn.microsoft.com/2784b925-678c-422c-ae78-84d2982c2b02">C/C++ Code Example: Retrieving Task Idle-wait Time</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/f7ad639a-4094-4621-9add-b89958c0bda4">IScheduledWorkItem::SetIdleWait</a>
 

 

