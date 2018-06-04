---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

