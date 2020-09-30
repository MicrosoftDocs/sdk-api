---
UID: NN:taskschd.IExecAction
title: IExecAction (taskschd.h)
description: Represents an action that executes a command-line operation.
helpviewer_keywords: ["IExecAction","IExecAction interface [Task Scheduler]","IExecAction interface [Task Scheduler]","described","execute action [Task Scheduler]","interface","taskschd.iexecaction","taskschd/IExecAction"]
old-location: taskschd\iexecaction.htm
tech.root: taskschd
ms.assetid: 46a4cd60-df23-4109-8a86-b7755a6922dd
ms.date: 12/05/2018
ms.keywords: IExecAction, IExecAction interface [Task Scheduler], IExecAction interface [Task Scheduler],described, execute action [Task Scheduler],interface, taskschd.iexecaction, taskschd/IExecAction
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
 - IExecAction
 - taskschd/IExecAction
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
 - IExecAction
---

# IExecAction interface


## -description

Represents an action that executes a command-line operation.

## -remarks

This action performs a command-line operation. For example, the action could run a script or launch an executable.

When reading or writing XML, an execution action is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-exec-actiongroup-element">Exec</a> element of the Task Scheduler schema.

If environment variables are used in the <a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path">Path</a>, <a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments">Arguments</a>, or <a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory">WorkingDirectory</a> properties, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched. Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>