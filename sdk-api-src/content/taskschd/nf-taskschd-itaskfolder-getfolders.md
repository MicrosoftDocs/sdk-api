---
UID: NF:taskschd.ITaskFolder.GetFolders
title: ITaskFolder::GetFolders
author: windows-sdk-content
description: Gets all the subfolders in the folder.
old-location: taskschd\itaskfolder_getfolders.htm
old-project: TaskSchd
ms.assetid: ee00a8be-52f5-4399-9a1f-18e06121a3da
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetFolders, GetFolders method [Task Scheduler], GetFolders method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],GetFolders method, ITaskFolder.GetFolders, ITaskFolder::GetFolders, taskschd.itaskfolder_getfolders, taskschd/ITaskFolder::GetFolders
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskFolder.GetFolders
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskFolder::GetFolders


## -description


Gets all the subfolders in the folder.


## -parameters




### -param flags [in]

This parameter is reserved for future use and must be set to 0.


### -param ppFolders [out]

The collection of subfolders in the folder.

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/1889a7e3-8fa2-4b96-9d55-656850f605da">ITaskFolderCollection</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

