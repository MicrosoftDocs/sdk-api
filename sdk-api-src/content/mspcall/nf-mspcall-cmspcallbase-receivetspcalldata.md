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

# CMSPCallBase::ReceiveTSPCallData


## -description


The 
<b>ReceiveTSPCallData</b> method is called by the MSP address object's 
<a href="https://msdn.microsoft.com/80b8e0aa-3361-4593-bec0-cbe9186c6c41">ReceiveTSPData</a> method to dispatch TSP data to the correct call. The call object should override this method to handle the TSP data according to whatever semantics have been defined for communication between this particular MSP and its corresponding TSP. The default implementation simply returns S_OK, which is sufficient for an MSP that does not handle any per-call TSP data.


## -parameters




### -param pBuffer

Pointer to buffer containing TSP data.


### -param dwSize

Size of the buffer, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>
 

 

