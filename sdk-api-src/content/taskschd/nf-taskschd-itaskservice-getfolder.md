---
UID: NF:taskschd.ITaskService.GetFolder
title: ITaskService::GetFolder (taskschd.h)
description: Gets a folder of registered tasks.
helpviewer_keywords: ["GetFolder","GetFolder method [Task Scheduler]","GetFolder method [Task Scheduler]","ITaskService interface","ITaskService interface [Task Scheduler]","GetFolder method","ITaskService.GetFolder","ITaskService::GetFolder","taskschd.itaskservice_getfolder","taskschd/ITaskService::GetFolder"]
old-location: taskschd\itaskservice_getfolder.htm
tech.root: taskschd
ms.assetid: 144b070f-43e9-40d6-8461-832abc7facd3
ms.date: 12/05/2018
ms.keywords: GetFolder, GetFolder method [Task Scheduler], GetFolder method [Task Scheduler],ITaskService interface, ITaskService interface [Task Scheduler],GetFolder method, ITaskService.GetFolder, ITaskService::GetFolder, taskschd.itaskservice_getfolder, taskschd/ITaskService::GetFolder
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
 - ITaskService::GetFolder
 - taskschd/ITaskService::GetFolder
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
 - ITaskService.GetFolder
---

# ITaskService::GetFolder


## -description

Gets a  folder of registered tasks.

## -parameters

### -param path [in]

The path to the folder to retrieve. Do not use a backslash following the last folder name in the path. The root task folder is specified with a backslash (\\). An example of a task folder path, under the root task folder,
 is \MyTaskFolder. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.

### -param ppFolder [out]

An <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a> interface for the requested folder.

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskservice">ITaskService</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>