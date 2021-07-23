---
UID: NF:taskschd.ITaskFolder.GetTask
title: ITaskFolder::GetTask (taskschd.h)
description: Gets a task at a specified location in a folder.
helpviewer_keywords: ["GetTask","GetTask method [Task Scheduler]","GetTask method [Task Scheduler]","ITaskFolder interface","ITaskFolder interface [Task Scheduler]","GetTask method","ITaskFolder.GetTask","ITaskFolder::GetTask","taskschd.itaskfolder_gettask","taskschd/ITaskFolder::GetTask"]
old-location: taskschd\itaskfolder_gettask.htm
tech.root: taskschd
ms.assetid: 01c32103-d65a-49ed-b12e-af2e865456e1
ms.date: 12/05/2018
ms.keywords: GetTask, GetTask method [Task Scheduler], GetTask method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],GetTask method, ITaskFolder.GetTask, ITaskFolder::GetTask, taskschd.itaskfolder_gettask, taskschd/ITaskFolder::GetTask
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
 - ITaskFolder::GetTask
 - taskschd/ITaskFolder::GetTask
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
 - ITaskFolder.GetTask
---

# ITaskFolder::GetTask


## -description

Gets a task at a specified location in a folder.

## -parameters

### -param path [in]

The path (location) to the task in a folder. The root task folder is specified with a backslash (\\). An example of a task folder path, under the root task folder,
 is \MyTaskFolder. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.

### -param ppTask [out]

The task at the specified location.

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask">IRegisteredTask</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>