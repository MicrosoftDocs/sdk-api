---
UID: NF:taskschd.ITaskFolder.GetTasks
title: ITaskFolder::GetTasks (taskschd.h)
description: Gets all the tasks in the folder.
helpviewer_keywords: ["GetTasks","GetTasks method [Task Scheduler]","GetTasks method [Task Scheduler]","ITaskFolder interface","ITaskFolder interface [Task Scheduler]","GetTasks method","ITaskFolder.GetTasks","ITaskFolder::GetTasks","taskschd.itaskfolder_gettasks","taskschd/ITaskFolder::GetTasks"]
old-location: taskschd\itaskfolder_gettasks.htm
tech.root: taskschd
ms.assetid: 2dcef962-d4b0-4fc9-845a-e33f020dba41
ms.date: 12/05/2018
ms.keywords: GetTasks, GetTasks method [Task Scheduler], GetTasks method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],GetTasks method, ITaskFolder.GetTasks, ITaskFolder::GetTasks, taskschd.itaskfolder_gettasks, taskschd/ITaskFolder::GetTasks
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
 - ITaskFolder::GetTasks
 - taskschd/ITaskFolder::GetTasks
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
 - ITaskFolder.GetTasks
---

# ITaskFolder::GetTasks


## -description

Gets all the tasks in the folder.

## -parameters

### -param flags [in]

Specifies whether to retrieve hidden tasks. Pass in TASK_ENUM_HIDDEN to retrieve all tasks in the folder including hidden tasks, and pass in 0 to retrieve all the tasks in the folder excluding the hidden tasks.

### -param ppTasks [out]

An <a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection">IRegisteredTaskCollection</a> collection of all the tasks in the folder.

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection">IRegisteredTaskCollection</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>