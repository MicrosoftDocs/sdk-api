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

# IScheduledWorkItem::SetIdleWait


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the minutes that the system must be idle before the <a href="w.htm">work item</a> can run.


## -parameters




### -param wIdleMinutes [in]

A value that specifies how long, in minutes, the system must remain idle before the work item can run.


### -param wDeadlineMinutes [in]

A value that specifies the maximum number of minutes that the Task Scheduler will wait for the idle-time period returned in <i>pwIdleMinutes</i>.


## -returns



The 
<b>SetIdleWait</b> method returns S_OK.




## -remarks



The idle time specified here is used in conjunction with <a href="i.htm">idle triggers</a> and <a href="i.htm">idle conditions</a>. For more information, see <a href="https://msdn.microsoft.com/1e480681-b77a-48fe-a732-dd1591eaa08d">Task Idle Conditions</a>. Idle triggers are event-based triggers that are not associated with a scheduled time. Idle conditions, in contrast, are associated with the scheduled start time for the task.

You specify idle triggers by setting the TASK_TRIGGER_TYPE member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> to TASK_EVENT_TRIGGER_ON_IDLE. The idle trigger is fired when the system becomes idle for the amount of time specified by <i>wIdleMinutes</i>.

You set idle conditions by calling 
<a href="https://msdn.microsoft.com/640ba3c7-ed9d-4c4c-82fd-34fc777172c2">IScheduledWorkItem::SetFlags</a>. If the TASK_FLAG_START_ONLY_IF_IDLE flag is set, the work item runs at its scheduled time only if the system becomes idle for the amount of time specified by <i>wIdleMinutes</i>. The Task Scheduler service will wait up to the number of minutes specified in <i>wDeadlineMinutes</i> past the scheduled start time to see if the system becomes idle.

Applications must call the <b>IPersistFile::Save</b> method after calling 
<b>SetIdleWait</b> to update the idle wait interval.


#### Examples

For an example of how to set the idle wait time when creating an idle trigger, see <a href="https://msdn.microsoft.com/d36a621c-4011-4c3d-b6f4-b56d1f50983c">Creating an Idle Trigger Example</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/72d53691-f2ea-4a20-8e85-f9db81f830cd">IScheduledWorkItem::GetIdleWait</a>
 

 

