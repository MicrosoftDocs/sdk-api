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

# ITimeTrigger interface


## -description


Represents a trigger that starts a task at a specific date and time.


## -remarks



The <a href="https://msdn.microsoft.com/95a62ae5-4eba-49df-a25f-0d1181772833">StartBoundary</a> element is a required element for time and calendar triggers (<a href="https://msdn.microsoft.com/bb467f36-47cd-4db4-97c4-60c09937caac">TimeTrigger</a> and <a href="https://msdn.microsoft.com/9b9218bf-222c-4ece-8b37-5c5d8b765015">CalendarTrigger</a>).

When reading or writing  XML for a task, an idle trigger is specified using the <a href="https://msdn.microsoft.com/bb467f36-47cd-4db4-97c4-60c09937caac">TimeTrigger</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

