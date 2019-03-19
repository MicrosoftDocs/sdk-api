---
UID: NN:taskschd.IIdleTrigger
title: IIdleTrigger (taskschd.h)
author: windows-sdk-content
description: Represents a trigger that starts a task when the computer goes into an idle state.
old-location: taskschd\iidletrigger.htm
tech.root: taskschd
ms.assetid: aca5305f-68fc-4211-9f71-3f572340e94d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IIdleTrigger, IIdleTrigger interface [Task Scheduler], IIdleTrigger interface [Task Scheduler],described, idle trigger [Task Scheduler],interface, taskschd.iidletrigger, taskschd/IIdleTrigger
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
 - IIdleTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIdleTrigger interface


## -description


Represents a trigger that starts a task when the computer goes into an idle state. For information about idle conditions, see <a href="https://msdn.microsoft.com/1e480681-b77a-48fe-a732-dd1591eaa08d">Task Idle Conditions</a>.


## -remarks



An idle trigger will only trigger a task action if the computer goes into an idle state after the start boundary of the trigger.


When creating your own XML for a task, an idle trigger is specified using the <a href="https://msdn.microsoft.com/c3e317b5-d1a7-46de-ace5-e066452583d3">IdleTrigger</a> element of the Task Scheduler schema.

If a task is triggered by an idle trigger, then the <a href="https://msdn.microsoft.com/fff7f954-4e57-42bf-ad86-5ddede94279c">WaitTimeout</a> property of the <a href="https://msdn.microsoft.com/a6bd9278-b9ac-4eb3-957a-5191cee12a6f">IIdleSettings</a> interface is ignored.

If the initial instance of a task with an idle trigger is still running, then the task is only launched once with no repetitions, even if multiple repetition is defined in the <a href="https://msdn.microsoft.com/8c3c5cc8-64aa-4706-a00a-0218fc1ae62b">Repetition</a> property. This behavior does not occur if the task stops by itself.




## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

