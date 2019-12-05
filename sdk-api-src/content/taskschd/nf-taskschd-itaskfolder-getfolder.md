---
UID: NF:taskschd.ITaskFolder.GetFolder
title: ITaskFolder::GetFolder (taskschd.h)
description: Gets a folder that contains tasks at a specified location.
old-location: taskschd\itaskfolder_getfolder.htm
tech.root: taskschd
ms.assetid: 62a0b946-ba06-46cf-bf38-e6774bdaae0a
ms.date: 12/05/2018
ms.keywords: GetFolder, GetFolder method [Task Scheduler], GetFolder method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],GetFolder method, ITaskFolder.GetFolder, ITaskFolder::GetFolder, taskschd.itaskfolder_getfolder, taskschd/ITaskFolder::GetFolder
ms.topic: method
f1_keywords:
- taskschd/ITaskFolder.GetFolder
dev_langs:
- c++
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
- ITaskFolder.GetFolder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskFolder::GetFolder


## -description


Gets a folder that contains tasks at a specified location.


## -parameters




### -param path [in]

The path (location) to the folder. Do not use a backslash following the last folder name in the path. The root task folder is specified with a backslash (\). An example of a task folder path, under the root task folder,
 is \MyTaskFolder. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.


### -param ppFolder [out]

The folder at the specified location.

Pass in a reference to a <b>NULL</b> <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskfolder">ITaskFolder</a>
 

 

