---
UID: NN:taskschd.IRegistrationInfo
title: IRegistrationInfo
author: windows-sdk-content
description: Provides the administrative information that can be used to describe the task.
old-location: taskschd\iregistrationinfo.htm
tech.root: TaskSchd
ms.assetid: e04f0c47-ab89-49e4-aac6-028d2555ecf1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IRegistrationInfo, IRegistrationInfo interface [Task Scheduler], IRegistrationInfo interface [Task Scheduler],described, registration information [Task Scheduler],interface, taskschd.iregistrationinfo, taskschd/IRegistrationInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRegistrationInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRegistrationInfo interface


## -description


Provides the administrative  information that can be used to describe the task. This information includes details such as a description of the task, the author of the task, the date the task is registered, and the security descriptor of the task.


## -remarks



Registration information can be used to identify a task through the Task Scheduler UI, or as search criteria when enumerating over the registered tasks.

When reading or writing XML for a task, registration information for the task is specified in the <a href="https://msdn.microsoft.com/f3961bad-e9a3-4626-87ed-9639d912717d">RegistrationInfo</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

