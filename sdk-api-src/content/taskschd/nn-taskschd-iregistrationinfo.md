---
UID: NN:taskschd.IRegistrationInfo
title: IRegistrationInfo (taskschd.h)
description: Provides the administrative information that can be used to describe the task.
helpviewer_keywords: ["IRegistrationInfo","IRegistrationInfo interface [Task Scheduler]","IRegistrationInfo interface [Task Scheduler]","described","registration information [Task Scheduler]","interface","taskschd.iregistrationinfo","taskschd/IRegistrationInfo"]
old-location: taskschd\iregistrationinfo.htm
tech.root: taskschd
ms.assetid: e04f0c47-ab89-49e4-aac6-028d2555ecf1
ms.date: 12/05/2018
ms.keywords: IRegistrationInfo, IRegistrationInfo interface [Task Scheduler], IRegistrationInfo interface [Task Scheduler],described, registration information [Task Scheduler],interface, taskschd.iregistrationinfo, taskschd/IRegistrationInfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRegistrationInfo
 - taskschd/IRegistrationInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IRegistrationInfo
---

# IRegistrationInfo interface


## -description

Provides the administrative  information that can be used to describe the task. This information includes details such as a description of the task, the author of the task, the date the task is registered, and the security descriptor of the task.

## -remarks

Registration information can be used to identify a task through the Task Scheduler UI, or as search criteria when enumerating over the registered tasks.

When reading or writing XML for a task, registration information for the task is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-registrationinfo-tasktype-element">RegistrationInfo</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>