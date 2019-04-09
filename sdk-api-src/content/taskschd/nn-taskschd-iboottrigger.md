---
UID: NN:taskschd.IBootTrigger
title: IBootTrigger (taskschd.h)
author: windows-sdk-content
description: Represents a trigger that starts a task when the system is started.
old-location: taskschd\iboottrigger.htm
tech.root: taskschd
ms.assetid: 8f186ee2-8d74-426c-9173-523a335422c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBootTrigger, IBootTrigger interface [Task Scheduler], IBootTrigger interface [Task Scheduler],described, boot trigger [Task Scheduler],interface, taskschd.iboottrigger, taskschd/IBootTrigger
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
 - IBootTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBootTrigger interface


## -description


Represents a trigger that starts a task when the system is started.


## -remarks



The Task Scheduler service is started when the operating system is booted, and boot trigger tasks are set to start when the Task Scheduler service starts.

Only a member of the Administrators group can create a task with a boot trigger.

When creating your own XML for a task, a boot trigger is specified using the <a href="https://msdn.microsoft.com/c6833547-0daf-4e8a-b8c5-b422827b1d96">BootTrigger</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/d4dbbfe5-bde9-4a1c-8e11-24cd1e14646c">Boot Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

