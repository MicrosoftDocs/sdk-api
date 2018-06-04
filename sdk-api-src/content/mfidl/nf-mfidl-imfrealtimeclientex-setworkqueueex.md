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

# IMFRealTimeClientEx::SetWorkQueueEx


## -description


Specifies the work queue that this object should use for asynchronous work items. 


## -parameters




### -param dwMultithreadedWorkQueueId

The work queue identifier.


### -param lWorkItemBasePriority

The base priority for work items.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The object should use the values of <i>dwMultithreadedWorkQueueId</i> and <i>lWorkItemBasePriority</i> when it queues new work items. Use the <a href="https://msdn.microsoft.com/C49818B3-83FF-40CE-B68A-F60F3277F7B8">MFPutWorkItem2</a> or <a href="https://msdn.microsoft.com/A29DC852-AF0F-4269-97FB-DA1F725E7C09">MFPutWorkItemEx2</a> function to queue the work item.




## -see-also




<a href="https://msdn.microsoft.com/EC5CDD23-B862-4DAE-AC01-4926C4FAD89A">IMFRealTimeClientEx</a>



<a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

