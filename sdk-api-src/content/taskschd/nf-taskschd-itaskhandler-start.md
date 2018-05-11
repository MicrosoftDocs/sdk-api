---
UID: NF:taskschd.ITaskHandler.Start
title: ITaskHandler::Start
author: windows-driver-content
description: Called to start the COM handler.
old-location: taskschd\itaskhandler_start.htm
old-project: TaskSchd
ms.assetid: e0a51387-e638-40ee-a4e4-edd7f3115975
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ITaskHandler interface [Task Scheduler],Start method, ITaskHandler.Start, ITaskHandler::Start, Start, Start method [Task Scheduler], Start method [Task Scheduler],ITaskHandler interface, taskschd.itaskhandler_start, taskschd/ITaskHandler::Start
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITaskHandler.Start
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskHandler::Start


## -description


Called to start the COM handler. This method must be implemented by the handler.


## -parameters




### -param pHandlerServices [in]

An <b>IUnkown</b> interface that is used to communicate back with the Task Scheduler.


### -param data [in]

The arguments that are required by the handler.  These arguments are defined in the <a href="https://msdn.microsoft.com/library/windows/hardware/mt427307">Data</a> property of the COM handler action.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When implementing this method, the handler should return control immediately to the Task Scheduler (starting its own thread if inproc).

After  the handler starts its processing, it can call the <a href="https://msdn.microsoft.com/3cab2b3b-7293-4d06-843f-9151d62d4950">UpdateStatus</a> method to indicate  its percentage of completion or call the <a href="https://msdn.microsoft.com/e6f7adf5-3cdb-4691-bc0a-682df7f019e2">TaskCompleted</a> method to indicate when the handler has completed its processing. These methods are provided by the <a href="https://msdn.microsoft.com/8b846be3-f05f-4d90-9865-da245c2bfdbf">ITaskHandlerStatus</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt427307">Data</a>



<a href="https://msdn.microsoft.com/ea3100d7-a80b-4487-9786-24124f2d72f1">ITaskHandler</a>



<a href="https://msdn.microsoft.com/8b846be3-f05f-4d90-9865-da245c2bfdbf">ITaskHandlerStatus</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/e6f7adf5-3cdb-4691-bc0a-682df7f019e2">TaskCompleted</a>



<a href="https://msdn.microsoft.com/3cab2b3b-7293-4d06-843f-9151d62d4950">UpdateStatus</a>
 

 

