---
UID: NF:taskschd.ITaskFolder.GetFolders
title: ITaskFolder::GetFolders
author: windows-sdk-content
description: Gets all the subfolders in the folder.
old-location: taskschd\itaskfolder_getfolders.htm
tech.root: taskschd
ms.assetid: ee00a8be-52f5-4399-9a1f-18e06121a3da
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFolders, GetFolders method [Task Scheduler], GetFolders method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],GetFolders method, ITaskFolder.GetFolders, ITaskFolder::GetFolders, taskschd.itaskfolder_getfolders, taskschd/ITaskFolder::GetFolders
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITaskFolder.GetFolders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

