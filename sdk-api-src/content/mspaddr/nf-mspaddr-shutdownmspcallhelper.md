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

# ShutdownMSPCallHelper function


## -description


The 
<b>ShutdownMSPCallHelper</b> helper template function is called in the derived class' implementation of 
<a href="https://msdn.microsoft.com/6527db85-cad8-4b0d-977a-9ab8b047e44e">ShutdownMSPCall</a>. It manipulates the passed-in aggregated TAPI call object Unknown pointer via dynamic casts to obtain a pointer to the inner MSP call object, and then calls the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method on the MSP call object (see below).


## -parameters




### -param pUnknown

Pointer to IUnknown on aggregated TAPI call object.


### -param ppCMSPCall

Pointer to templated MSP call class, type implementation dependent.


### -param param

TBD




## -see-also




<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a>
 

 

