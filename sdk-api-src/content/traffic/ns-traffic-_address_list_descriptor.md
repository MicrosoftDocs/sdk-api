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

# _ADDRESS_LIST_DESCRIPTOR structure


## -description


The 
<b>ADDRESS_LIST_DESCRIPTOR</b> structure provides network address descriptor information for a given interface. For point-to-point media such as WAN connections, the list is a pair of addresses, the first of which is always the local or source address, the second of which is the remote or destination address. Note that the members of 
<b>ADDRESS_LIST_DESCRIPTOR</b> are defined in Ntddndis.h.


## -struct-fields




### -field MediaType

Media type of the interface.


### -field AddressList

Pointer to the address list for the interface. The <b>NETWORK_ADDRESS_LIST</b> structure is defined in Ntddndis.h.


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>
 

 

