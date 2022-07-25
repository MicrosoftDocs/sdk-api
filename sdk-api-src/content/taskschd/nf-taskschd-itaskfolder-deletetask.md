---
UID: NF:taskschd.ITaskFolder.DeleteTask
title: ITaskFolder::DeleteTask (taskschd.h)
description: Deletes a task from the folder.
helpviewer_keywords: ["DeleteTask","DeleteTask method [Task Scheduler]","DeleteTask method [Task Scheduler]","ITaskFolder interface","ITaskFolder interface [Task Scheduler]","DeleteTask method","ITaskFolder.DeleteTask","ITaskFolder::DeleteTask","taskschd.itaskfolder_deletetask","taskschd/ITaskFolder::DeleteTask"]
old-location: taskschd\itaskfolder_deletetask.htm
tech.root: taskschd
ms.assetid: 5b929abd-c40a-4f6b-9a0b-702d2f26f1fe
ms.date: 12/05/2018
ms.keywords: DeleteTask, DeleteTask method [Task Scheduler], DeleteTask method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],DeleteTask method, ITaskFolder.DeleteTask, ITaskFolder::DeleteTask, taskschd.itaskfolder_deletetask, taskschd/ITaskFolder::DeleteTask
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
 - ITaskFolder::DeleteTask
 - taskschd/ITaskFolder::DeleteTask
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
 - ITaskFolder.DeleteTask
---

# ITaskFolder::DeleteTask


## -description

Deletes a task from the folder.

## -parameters

### -param name [in]

The name of the task that is specified when the task was registered. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.

### -param flags [in]

Not supported.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>