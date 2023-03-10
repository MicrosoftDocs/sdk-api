---
UID: NF:taskschd.ITaskFolder.GetFolders
title: ITaskFolder::GetFolders (taskschd.h)
description: Gets all the subfolders in the folder.
helpviewer_keywords: ["GetFolders","GetFolders method [Task Scheduler]","GetFolders method [Task Scheduler]","ITaskFolder interface","ITaskFolder interface [Task Scheduler]","GetFolders method","ITaskFolder.GetFolders","ITaskFolder::GetFolders","taskschd.itaskfolder_getfolders","taskschd/ITaskFolder::GetFolders"]
old-location: taskschd\itaskfolder_getfolders.htm
tech.root: taskschd
ms.assetid: ee00a8be-52f5-4399-9a1f-18e06121a3da
ms.date: 12/05/2018
ms.keywords: GetFolders, GetFolders method [Task Scheduler], GetFolders method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],GetFolders method, ITaskFolder.GetFolders, ITaskFolder::GetFolders, taskschd.itaskfolder_getfolders, taskschd/ITaskFolder::GetFolders
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
 - ITaskFolder::GetFolders
 - taskschd/ITaskFolder::GetFolders
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
 - ITaskFolder.GetFolders
---

# ITaskFolder::GetFolders


## -description

Gets all the subfolders in the folder.

## -parameters

### -param flags [in]

This parameter is reserved for future use and must be set to 0.

### -param ppFolders [out]

The collection of subfolders in the folder.

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfoldercollection">ITaskFolderCollection</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>