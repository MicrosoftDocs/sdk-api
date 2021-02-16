---
UID: NF:taskschd.IRunningTask.get_CurrentAction
title: IRunningTask::get_CurrentAction (taskschd.h)
description: Gets the name of the current action that the running task is performing.
helpviewer_keywords: ["CurrentAction property [Task Scheduler]","CurrentAction property [Task Scheduler]","IRunningTask interface","IRunningTask interface [Task Scheduler]","CurrentAction property","IRunningTask.CurrentAction","IRunningTask.get_CurrentAction","IRunningTask::CurrentAction","IRunningTask::get_CurrentAction","get_CurrentAction","taskschd.irunningtask_currentaction","taskschd/IRunningTask::CurrentAction","taskschd/IRunningTask::get_CurrentAction"]
old-location: taskschd\irunningtask_currentaction.htm
tech.root: taskschd
ms.assetid: 52b58477-e968-4c76-835d-02ed63cef641
ms.date: 12/05/2018
ms.keywords: CurrentAction property [Task Scheduler], CurrentAction property [Task Scheduler],IRunningTask interface, IRunningTask interface [Task Scheduler],CurrentAction property, IRunningTask.CurrentAction, IRunningTask.get_CurrentAction, IRunningTask::CurrentAction, IRunningTask::get_CurrentAction, get_CurrentAction, taskschd.irunningtask_currentaction, taskschd/IRunningTask::CurrentAction, taskschd/IRunningTask::get_CurrentAction
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
 - IRunningTask::get_CurrentAction
 - taskschd/IRunningTask::get_CurrentAction
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
 - IRunningTask.CurrentAction
 - IRunningTask.get_CurrentAction
---

# IRunningTask::get_CurrentAction


## -description

Gets the name of the current action that the running task is performing.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/taskschd/nf-taskschd-irunningtask-refresh">IRunningTask::Refresh</a> method is called before the property value is returned.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtask">IRunningTask</a>