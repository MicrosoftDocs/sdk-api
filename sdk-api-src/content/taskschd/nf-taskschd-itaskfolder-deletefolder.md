---
UID: NF:taskschd.ITaskFolder.DeleteFolder
title: ITaskFolder::DeleteFolder
author: windows-sdk-content
description: Deletes a subfolder from the parent folder.
old-location: taskschd\itaskfolder_deletefolder.htm
old-project: TaskSchd
ms.assetid: 7758afc5-73d8-456c-98a9-89e4b7ad42b9
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DeleteFolder, DeleteFolder method [Task Scheduler], DeleteFolder method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],DeleteFolder method, ITaskFolder.DeleteFolder, ITaskFolder::DeleteFolder, taskschd.itaskfolder_deletefolder, taskschd/ITaskFolder::DeleteFolder
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
 - ITaskFolder.DeleteFolder
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskFolder::DeleteFolder


## -description


Deletes a subfolder from the parent folder.


## -parameters




### -param subFolderName




### -param flags [in]

Not supported.


#### - folderName [in]

The name of the subfolder to be removed. The root task folder is specified with a backslash (\). This parameter can be a relative path to the folder you want to delete. An example of a task folder path, under the root task folder,
 is \MyTaskFolder. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

