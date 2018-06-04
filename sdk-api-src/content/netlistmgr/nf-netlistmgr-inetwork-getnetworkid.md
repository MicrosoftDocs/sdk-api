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

# INetwork::GetNetworkId


## -description


The <b>GetNetworkId</b> method returns the unique identifier of a network.


## -parameters




### -param pgdGuidNetworkId [out]

Pointer to a GUID that specifies the network ID.


## -returns



Returns S_OK if the method succeeds.




## -remarks



The caller is responsible for allocating the buffer pointed to by <i>pgdGuidNetworkId</i>. This buffer must be large enough to hold a GUID. 

Calling  <b>GetNetworkId</b> will return S_OK even if the network requested has been deleted.




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>
 

 

