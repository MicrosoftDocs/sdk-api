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

# IWSDiscoveryPublisherNotify::ResolveHandler


## -description


Is called when a <a href="https://msdn.microsoft.com/b963bd2a-47cb-4f8d-8272-a586e6d6a047">Resolve</a> is received by the discovery publisher.


## -parameters




### -param pSoap [in]

Pointer to a <a href="https://msdn.microsoft.com/e5352a78-3ece-45d3-bf95-2d922065e3d5">WSD_SOAP_MESSAGE</a> structure that contains the Resolve message received by the discovery publisher.


### -param pMessageParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a> interface that contains transport information associated with the received message.


## -returns



The return value is not meaningful. An implementer should return S_OK.




## -remarks



<b>ResolveHandler</b> is called whenever a Resolve is received by the discovery publisher. It is the responsibility of the callback interface to then call <a href="https://msdn.microsoft.com/f01a17ce-2a87-4f11-81d3-a94743b309ab">MatchResolve</a> or <a href="https://msdn.microsoft.com/0eba744c-c335-4b82-95f0-6142cfedad09">MatchResolveEx</a> with host information to determine whether or not the received Resolve matches the host.




## -see-also




<a href="https://msdn.microsoft.com/6e7e0ab8-dffe-47c2-916c-a6734eb4ac44">IWSDiscoveryPublisherNotify</a>
 

 

