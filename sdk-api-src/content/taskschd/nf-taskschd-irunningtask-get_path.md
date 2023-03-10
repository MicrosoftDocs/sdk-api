---
UID: NF:taskschd.IRunningTask.get_Path
title: IRunningTask::get_Path (taskschd.h)
description: Gets the path to where the task is stored.
helpviewer_keywords: ["IRunningTask interface [Task Scheduler]","Path property","IRunningTask.Path","IRunningTask.get_Path","IRunningTask::Path","IRunningTask::get_Path","Path property [Task Scheduler]","Path property [Task Scheduler]","IRunningTask interface","get_Path","taskschd.irunningtask_path","taskschd/IRunningTask::Path","taskschd/IRunningTask::get_Path"]
old-location: taskschd\irunningtask_path.htm
tech.root: taskschd
ms.assetid: 8c364628-63dd-4018-9eeb-6acab265c144
ms.date: 12/05/2018
ms.keywords: IRunningTask interface [Task Scheduler],Path property, IRunningTask.Path, IRunningTask.get_Path, IRunningTask::Path, IRunningTask::get_Path, Path property [Task Scheduler], Path property [Task Scheduler],IRunningTask interface, get_Path, taskschd.irunningtask_path, taskschd/IRunningTask::Path, taskschd/IRunningTask::get_Path
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
 - IRunningTask::get_Path
 - taskschd/IRunningTask::get_Path
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
 - IRunningTask.Path
 - IRunningTask.get_Path
---

# IRunningTask::get_Path


## -description

Gets the path to where the task is stored.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/taskschd/nf-taskschd-irunningtask-refresh">IRunningTask::Refresh</a> method is called before the property value is returned.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtask">IRunningTask</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>