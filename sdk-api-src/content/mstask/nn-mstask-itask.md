---
UID: NN:mstask.ITask
title: ITask (mstask.h)
description: Provides the methods for running tasks, getting or setting task information, and terminating tasks. It is derived from the IScheduledWorkItem interface and inherits all the methods of that interface.
helpviewer_keywords: ["ITask","ITask interface [Task Scheduler]","ITask interface [Task Scheduler]","described","_msb_itask","mstask/ITask","taskschd.itask"]
old-location: taskschd\itask.htm
tech.root: taskschd
ms.assetid: 84a70dd0-43cb-42be-8360-35263bf1afb8
ms.date: 12/05/2018
ms.keywords: ITask, ITask interface [Task Scheduler], ITask interface [Task Scheduler],described, _msb_itask, mstask/ITask, taskschd.itask
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - ITask
 - mstask/ITask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - ITask
---

# ITask interface


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for running tasks, getting or setting task information, and terminating tasks. It is derived from the 
<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a> interface and inherits all the methods of that interface.

## -inheritance

The <b>ITask</b> interface inherits from <a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>. <b>ITask</b> also has these types of members:

## -remarks

<b>ITask</b> is the primary interface of the <a href="/windows/desktop/TaskSchd/t">task trigger object</a>. To create a task object, call 
<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-activate">ITaskScheduler::Activate</a> for existing tasks or 
<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-newworkitem">ITaskScheduler::NewWorkItem</a> for new tasks.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/c-c-code-example-terminating-a-task">C/C++ Code Example: Terminating a Task</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-activate">ITaskScheduler::Activate</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-newworkitem">ITaskScheduler::NewWorkItem</a>
