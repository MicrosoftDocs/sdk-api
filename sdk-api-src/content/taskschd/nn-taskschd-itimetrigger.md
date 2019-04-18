---
UID: NN:taskschd.ITimeTrigger
title: ITimeTrigger (taskschd.h)
author: windows-sdk-content
description: Represents a trigger that starts a task at a specific date and time.
old-location: taskschd\itimetrigger.htm
tech.root: taskschd
ms.assetid: 4ebd5470-0801-42ff-a0c2-4d1e7f7ee365
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITimeTrigger, ITimeTrigger interface [Task Scheduler], ITimeTrigger interface [Task Scheduler],described, taskschd.itimetrigger, taskschd/ITimeTrigger, time trigger [Task Scheduler],interface
ms.topic: interface
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITimeTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

