---
UID: NN:taskschd.IEventTrigger
title: IEventTrigger
author: windows-sdk-content
description: Represents a trigger that starts a task when a system event occurs.
old-location: taskschd\ieventtrigger.htm
old-project: taskschd
ms.assetid: 23b7ecb9-d2bb-441a-8c93-126c833f99b9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEventTrigger, IEventTrigger interface [Task Scheduler], IEventTrigger interface [Task Scheduler],described, event trigger [Task Scheduler],interface, taskschd.ieventtrigger, taskschd/IEventTrigger
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: taskschd.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IEventTrigger
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEventTrigger interface


## -description


Represents a trigger that starts a task when a system event occurs.


## -remarks



A maximum of 500 tasks with event subscriptions can be created. An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.

When reading or writing your own XML for a task, an event trigger is specified using the <a href="https://msdn.microsoft.com/8faffc04-1ad2-499d-bcdf-bc28f64b8aa8">EventTrigger</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/cacc1b72-7c58-4117-b204-ddb3a312bb08">Event Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7eea143b-d2f8-44d2-a3ec-8328a0bc69ef">IRepetitionPattern</a>



<a href="https://msdn.microsoft.com/329232de-6068-4757-b567-3ce4d2c5ba4a">IShowMessageAction</a>



<a href="https://msdn.microsoft.com/440dc70b-02de-4974-ad2a-462491d12775">ITaskNamedValueCollection</a>



<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/489015a1-5a3c-4994-aa1f-bc02dfff149d">TASK_TRIGGER_TYPE2</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

