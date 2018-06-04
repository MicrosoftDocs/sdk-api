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

# _WSAPROTOCOLCHAIN structure


## -description



			The 
<b>WSAPROTOCOLCHAIN</b> structure contains a counted list of Catalog Entry identifiers that comprise a protocol chain. 


## -struct-fields




### -field ChainLen

Length of the chain, in bytes. The following settings apply: 




Setting <b>ChainLen</b> to zero indicates a layered protocol

Setting <b>ChainLen</b> to one indicates a base protocol

Setting <b>ChainLen</b> to greater than one indicates a protocol chain


### -field ChainEntries

Array of protocol chain entries.


## -remarks



If the length of the chain is larger than 1, this structure represents a protocol chain which consists of one or more layered protocols on top of a base protocol. The corresponding Catalog Entry IDs are in the ProtocolChain.ChainEntries array starting with the layered protocol at the top (the zeroth element in the ProtocolChain.ChainEntries array) and ending with the base protocol. Refer to Windows Sockets 2 Service Provider Interface for more information on protocol chains.




## -see-also




<a href="https://msdn.microsoft.com/928b6937-41a3-4268-a3bc-14c9e04870e4">WSAEnumProtocols</a>
 

 

