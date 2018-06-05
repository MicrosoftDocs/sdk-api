---
UID: NF:taskschd.ITaskHandlerStatus.TaskCompleted
title: ITaskHandlerStatus::TaskCompleted
author: windows-sdk-content
description: Tells the Task Scheduler that the COM handler is completed.
old-location: taskschd\itaskhandlerstatus_taskcompleted.htm
old-project: TaskSchd
ms.assetid: e6f7adf5-3cdb-4691-bc0a-682df7f019e2
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ITaskHandlerStatus interface [Task Scheduler],TaskCompleted method, ITaskHandlerStatus.TaskCompleted, ITaskHandlerStatus::TaskCompleted, TaskCompleted, TaskCompleted method [Task Scheduler], TaskCompleted method [Task Scheduler],ITaskHandlerStatus interface, taskschd.itaskhandlerstatus_taskcompleted, taskschd/ITaskHandlerStatus::TaskCompleted
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITaskHandlerStatus.TaskCompleted
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskHandlerStatus::TaskCompleted


## -description


Tells the Task Scheduler that the COM handler is completed.


## -parameters




### -param taskErrCode [in]

The error code that the Task Scheduler will raise as an event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8b846be3-f05f-4d90-9865-da245c2bfdbf">ITaskHandlerStatus</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

