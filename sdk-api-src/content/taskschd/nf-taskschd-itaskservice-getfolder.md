---
UID: NF:taskschd.ITaskService.GetFolder
title: ITaskService::GetFolder
author: windows-sdk-content
description: Gets a folder of registered tasks.
old-location: taskschd\itaskservice_getfolder.htm
old-project: TaskSchd
ms.assetid: 144b070f-43e9-40d6-8461-832abc7facd3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetFolder, GetFolder method [Task Scheduler], GetFolder method [Task Scheduler],ITaskService interface, ITaskService interface [Task Scheduler],GetFolder method, ITaskService.GetFolder, ITaskService::GetFolder, taskschd.itaskservice_getfolder, taskschd/ITaskService::GetFolder
ms.prod: windows
ms.technology: windows-sdk
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
 - ITaskService.GetFolder
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskService::GetFolder


## -description


Gets a  folder of registered tasks.


## -parameters




### -param path [in]

The path to the folder to retrieve. Do not use a backslash following the last folder name in the path. The root task folder is specified with a backslash (\). An example of a task folder path, under the root task folder,
 is \MyTaskFolder. The '.' character  cannot be used to specify the current task folder  and the '..' characters cannot be used to specify the parent task folder in the path.


### -param ppFolder [out]

An <a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a> interface for the requested folder.

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/da0cc808-b284-4d10-be61-d96c5e07d0a8">ITaskFolder</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2459aaae-4c3a-458a-ad2c-bfff3a0322d3">ITaskService</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

