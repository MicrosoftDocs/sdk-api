---
UID: NF:taskschd.ITaskHandlerStatus.TaskCompleted
title: ITaskHandlerStatus::TaskCompleted (taskschd.h)
description: Tells the Task Scheduler that the COM handler is completed.
helpviewer_keywords: ["ITaskHandlerStatus interface [Task Scheduler]","TaskCompleted method","ITaskHandlerStatus.TaskCompleted","ITaskHandlerStatus::TaskCompleted","TaskCompleted","TaskCompleted method [Task Scheduler]","TaskCompleted method [Task Scheduler]","ITaskHandlerStatus interface","taskschd.itaskhandlerstatus_taskcompleted","taskschd/ITaskHandlerStatus::TaskCompleted"]
old-location: taskschd\itaskhandlerstatus_taskcompleted.htm
tech.root: taskschd
ms.assetid: e6f7adf5-3cdb-4691-bc0a-682df7f019e2
ms.date: 12/05/2018
ms.keywords: ITaskHandlerStatus interface [Task Scheduler],TaskCompleted method, ITaskHandlerStatus.TaskCompleted, ITaskHandlerStatus::TaskCompleted, TaskCompleted, TaskCompleted method [Task Scheduler], TaskCompleted method [Task Scheduler],ITaskHandlerStatus interface, taskschd.itaskhandlerstatus_taskcompleted, taskschd/ITaskHandlerStatus::TaskCompleted
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
 - ITaskHandlerStatus::TaskCompleted
 - taskschd/ITaskHandlerStatus::TaskCompleted
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
 - ITaskHandlerStatus.TaskCompleted
---

# ITaskHandlerStatus::TaskCompleted


## -description

Tells the Task Scheduler that the COM handler is completed.

## -parameters

### -param taskErrCode [in]

The error code that the Task Scheduler will raise as an event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus">ITaskHandlerStatus</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>