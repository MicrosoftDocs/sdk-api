---
UID: NF:taskschd.ITaskFolder.DeleteFolder
title: ITaskFolder::DeleteFolder (taskschd.h)
author: windows-sdk-content
description: Deletes a subfolder from the parent folder.
old-location: taskschd\itaskfolder_deletefolder.htm
tech.root: taskschd
ms.assetid: 7758afc5-73d8-456c-98a9-89e4b7ad42b9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteFolder, DeleteFolder method [Task Scheduler], DeleteFolder method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],DeleteFolder method, ITaskFolder.DeleteFolder, ITaskFolder::DeleteFolder, taskschd.itaskfolder_deletefolder, taskschd/ITaskFolder::DeleteFolder
ms.topic: method
f1_keywords: 
 - "taskschd/ITaskFolder.DeleteFolder"
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
 - ITaskFolder.DeleteFolder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskFolder::DeleteFolder


## -description


Deletes a subfolder from the parent folder.


## -parameters




### -param subFolderName [in]

The name of the subfolder to be removed. The root task folder is specified with a backslash (\). This parameter can be a relative path to the folder you want to delete. An example of a task folder path, under the root task folder,
 is \MyTaskFolder. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.


### -param flags [in]

Not supported.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

