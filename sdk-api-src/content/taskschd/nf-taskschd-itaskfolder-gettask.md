---
UID: NF:taskschd.ITaskFolder.GetTask
title: ITaskFolder::GetTask
author: windows-sdk-content
description: Gets a task at a specified location in a folder.
old-location: taskschd\itaskfolder_gettask.htm
tech.root: TaskSchd
ms.assetid: 01c32103-d65a-49ed-b12e-af2e865456e1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetTask, GetTask method [Task Scheduler], GetTask method [Task Scheduler],ITaskFolder interface, ITaskFolder interface [Task Scheduler],GetTask method, ITaskFolder.GetTask, ITaskFolder::GetTask, taskschd.itaskfolder_gettask, taskschd/ITaskFolder::GetTask
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
 - ITaskFolder.GetTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- taskschd.h
: 
- ITaskFolder.GetTask
: 
---

# ITaskFolder::GetTask


## -description


Gets a task at a specified location in a folder.


## -parameters




### -param path [in]

The path (location) to the task in a folder. The root task folder is specified with a backslash (\). An example of a task folder path, under the root task folder,
 is \MyTaskFolder. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.


### -param ppTask [out]

The task at the specified location.

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/3743d012-ad7c-402f-8859-939bb01ee447">IRegisteredTask</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a>
 

 

