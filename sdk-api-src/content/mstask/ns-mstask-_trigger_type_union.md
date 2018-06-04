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

# _TRIGGER_TYPE_UNION structure


## -description



			
			
		Defines the invocation schedule of the trigger within the <b>Type</b> member of a 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure.


## -struct-fields




### -field Daily

A 
<a href="https://msdn.microsoft.com/4dbab308-fd1c-4be4-84f6-c12f751ab29e">DAILY</a> structure that specifies the number of days between invocations of a task.


### -field Weekly

A 
<a href="https://msdn.microsoft.com/e2c14738-846c-485e-a564-d8e738ca61a2">WEEKLY</a> structure that specifies the number of weeks between invocations of a task, and day(s) of the week the task will run.


### -field MonthlyDate

A 
<a href="https://msdn.microsoft.com/51d010c9-4e16-49b7-8034-dfb27761c6a6">MONTHLYDATE</a> structure that specifies the month(s) and day(s) of the month a task will run.


### -field MonthlyDOW

A 
<a href="https://msdn.microsoft.com/1f353611-0542-4534-91bf-4a76f41c9c9d">MONTHLYDOW</a> structure that specifies the day(s) of the year a task runs by month(s), week of month, and day(s) of week.


## -remarks



The <b>TriggerType</b> member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure defines which fields of this union are used.




## -see-also




<a href="https://msdn.microsoft.com/4dbab308-fd1c-4be4-84f6-c12f751ab29e">DAILY</a>



<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/51d010c9-4e16-49b7-8034-dfb27761c6a6">MONTHLYDATE</a>



<a href="https://msdn.microsoft.com/1f353611-0542-4534-91bf-4a76f41c9c9d">MONTHLYDOW</a>



<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>



<a href="https://msdn.microsoft.com/e2c14738-846c-485e-a564-d8e738ca61a2">WEEKLY</a>
 

 

