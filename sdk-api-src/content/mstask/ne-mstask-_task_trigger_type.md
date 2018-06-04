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

# _TASK_TRIGGER_TYPE enumeration


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the  <a href="https://msdn.microsoft.com/d59f017e-df32-4826-954d-9ba338282d0d">Task Scheduler 2.0 Enumerated Types</a> instead.] ]

Defines the types of <a href="t.htm">triggers</a> associated with a task.


## -enum-fields




### -field TASK_TIME_TRIGGER_ONCE

Trigger is set to run the task a single time. 




When this value is specified, the <b>Type</b> member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure is ignored.


### -field TASK_TIME_TRIGGER_DAILY

Trigger is set to run the task on a daily interval. 




When this value is specified, the 
<b>DAILY</b> member of the 
<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a> structure is used.


### -field TASK_TIME_TRIGGER_WEEKLY

Trigger is set to run the work item on specific days of a specific week of a specific month. 




When this value is specified, the 
<b>WEEKLY</b> member of the 
<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a> structure is used.


### -field TASK_TIME_TRIGGER_MONTHLYDATE

Trigger is set to run the task on a specific day(s) of the month. 




When this value is specified, the 
<b>MONTHLYDATE</b> member of the 
<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a> structure is used.


### -field TASK_TIME_TRIGGER_MONTHLYDOW

Trigger is set to run the task on specific days, weeks, and months. 




When this value is specified, the 
<b>MONTHLYDOW</b> member of the 
<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a> structure is used.


### -field TASK_EVENT_TRIGGER_ON_IDLE

Trigger is set to run the task if the system remains idle for the amount of time specified by the <a href="i.htm">idle wait time</a> of the task. 




When this value is specified, the <b>wStartHour</b>, <b>wStartMinute</b>, and <b>Type</b> member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure are ignored.


### -field TASK_EVENT_TRIGGER_AT_SYSTEMSTART

Trigger is set to run the task at system startup. 




When this value is specified, the <b>Type</b> member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure is ignored.


### -field TASK_EVENT_TRIGGER_AT_LOGON

Trigger is set to run the task when a user logs on. 




When this value is specified, the <b>Type</b> member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure is ignored.


## -remarks



The constants defined here are used in the <b>TriggerType</b> member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/f7ad639a-4094-4621-9add-b89958c0bda4">IScheduledWorkItem::SetIdleWait</a>



<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a>



<a href="https://msdn.microsoft.com/489015a1-5a3c-4994-aa1f-bc02dfff149d">TASK_TRIGGER_TYPE2</a>



<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

