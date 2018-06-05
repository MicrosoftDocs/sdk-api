---
UID: NN:taskschd.IIdleSettings
title: IIdleSettings
author: windows-sdk-content
description: Specifies how the Task Scheduler performs tasks when the computer is in an idle condition.
old-location: taskschd\iidlesettings.htm
old-project: TaskSchd
ms.assetid: a6bd9278-b9ac-4eb3-957a-5191cee12a6f
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IIdleSettings, IIdleSettings interface [Task Scheduler], IIdleSettings interface [Task Scheduler],described, taskschd.iidlesettings, taskschd/IIdleSettings
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IIdleSettings
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IIdleSettings interface


## -description


Specifies how the Task Scheduler performs tasks when the computer is in an idle condition. For information about idle conditions, see <a href="https://msdn.microsoft.com/1e480681-b77a-48fe-a732-dd1591eaa08d">Task Idle Conditions</a>.


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/23d57417-95a9-42e3-904c-7f0859fcda7c">IdleSettings</a> element of the Task Scheduler schema.

If a task is triggered by an idle trigger, then the <a href="https://msdn.microsoft.com/fff7f954-4e57-42bf-ad86-5ddede94279c">WaitTimeout</a> property of the <b>IIdleSettings</b> interface is ignored.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

