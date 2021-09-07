---
UID: NF:taskschd.ITaskFolder.CreateFolder
title: ITaskFolder::CreateFolder (taskschd.h)
description: Creates a folder for related tasks.
helpviewer_keywords: ["CreateFolder","CreateFolder method [Task Scheduler]","CreateFolder method [Task Scheduler]","ITaskFolder interface","ITaskFolder interface [Task Scheduler]","CreateFolder method","ITaskFolder.CreateFolder","ITaskFolder::CreateFolder","taskschd.itaskfolder_createfolder","taskschd/ITaskFolder::CreateFolder"]
old-location: taskschd\itaskfolder_createfolder.htm
tech.root: taskschd
ms.assetid: da0f2420-b1a0-4359-aa05-ddf1f2a35118
ms.date: 12/05/2018
ms.keywords: CreateFolder, CreateFolder method [Task Scheduler], CreateFolder method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],CreateFolder method, ITaskFolder.CreateFolder, ITaskFolder::CreateFolder, taskschd.itaskfolder_createfolder, taskschd/ITaskFolder::CreateFolder
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
 - ITaskFolder::CreateFolder
 - taskschd/ITaskFolder::CreateFolder
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
 - ITaskFolder.CreateFolder
---

# ITaskFolder::CreateFolder


## -description

Creates a folder for related tasks.

## -parameters

### -param subFolderName [in]

The name used to identify the folder. If "FolderName\SubFolder1\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist. This parameter can be a relative path to the current <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a> instance. The root task folder is specified with a backslash (\\). An example of a task folder path, under the root task folder,
 is \MyTaskFolder. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.

### -param sddl [in]

The security descriptor associated with the folder, in the form of a VT_BSTR in SDDL_REVISION_1 format.

### -param ppFolder [out]

An <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a> interface that represents the new subfolder.

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To retrieve the subfolders of the parent folder, use the <a href="/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-getfolders">GetFolders</a> method.

The <b>CreateFolder</b> method will return 0x800700b7 if the folder that you are trying to create already exists.

Specifying an invalid security descriptor in the <i>sddl</i> parameter will cause this method to return <b>E_INVALIDARG</b>.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>