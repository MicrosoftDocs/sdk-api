---
UID: NF:taskschd.ITaskFolder.CreateFolder
title: ITaskFolder::CreateFolder
author: windows-sdk-content
description: Creates a folder for related tasks.
old-location: taskschd\itaskfolder_createfolder.htm
tech.root: taskschd
ms.assetid: da0f2420-b1a0-4359-aa05-ddf1f2a35118
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFolder, CreateFolder method [Task Scheduler], CreateFolder method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],CreateFolder method, ITaskFolder.CreateFolder, ITaskFolder::CreateFolder, taskschd.itaskfolder_createfolder, taskschd/ITaskFolder::CreateFolder
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskFolder.CreateFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskFolder::CreateFolder


## -description


Creates a folder for related tasks.


## -parameters




### -param subFolderName [in]

The name used to identify the folder. If "FolderName\SubFolder1\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist. This parameter can be a relative path to the current <a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a> instance. The root task folder is specified with a backslash (\). An example of a task folder path, under the root task folder,
 is \MyTaskFolder. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.


### -param sddl [in]

The security descriptor associated with the folder, in the form of a VT_BSTR in SDDL_REVISION_1 format.


### -param ppFolder [out]

An <a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a> interface that represents the new subfolder.

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To retrieve the subfolders of the parent folder, use the <a href="https://msdn.microsoft.com/ee00a8be-52f5-4399-9a1f-18e06121a3da">GetFolders</a> method.

The <b>CreateFolder</b> method will return 0x800700b7 if the folder that you are trying to create already exists.

Specifying an invalid security descriptor in the <i>sddl</i> parameter will cause this method to return <b>E_INVALIDARG</b>.




## -see-also




<a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

