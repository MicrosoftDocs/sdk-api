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

# RtwqSetDeadline function


## -description


Sets a deadline by which the work in a work queue must be completed.


## -parameters




### -param workQueueId [in]

The identifier for the work queue. The identifier is returned by the <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a> function. 


### -param deadlineInHNS

TBD


### -param pRequest [in, out]

Receives a handle to the request that can be used to cancel the request by calling <a href="https://msdn.microsoft.com/4128B655-AFF9-4AEF-8EDB-A6DC8DA05FE9">RtwqCancelDeadline</a>.


#### - llDeadline [in]

 The deadline for the work in the queue to be completed, in milliseconds.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Update a deadline by creating a new deadline and releasing the old one.

Cancel a deadline by calling <a href="https://msdn.microsoft.com/4128B655-AFF9-4AEF-8EDB-A6DC8DA05FE9">RtwqCancelDeadline</a>.




## -see-also




<a href="https://msdn.microsoft.com/4128B655-AFF9-4AEF-8EDB-A6DC8DA05FE9">RtwqCancelDeadline</a>
 

 

