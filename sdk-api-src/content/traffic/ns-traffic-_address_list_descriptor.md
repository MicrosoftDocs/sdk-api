---
UID: NS:traffic._ADDRESS_LIST_DESCRIPTOR
title: "_ADDRESS_LIST_DESCRIPTOR"
author: windows-sdk-content
description: The ADDRESS_LIST_DESCRIPTOR structure provides network address descriptor information for a given interface.
old-location: qos\address_list_descriptor.htm
old-project: QOS
ms.assetid: d891b82a-999e-4d59-a676-a90648e17699
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PADDRESS_LIST_DESCRIPTOR, ADDRESS_LIST_DESCRIPTOR, ADDRESS_LIST_DESCRIPTOR structure [QOS], PADDRESS_LIST_DESCRIPTOR, PADDRESS_LIST_DESCRIPTOR structure pointer [QOS], _ADDRESS_LIST_DESCRIPTOR, _gqos_address_list_descriptor, qos.address_list_descriptor, traffic/ADDRESS_LIST_DESCRIPTOR, traffic/PADDRESS_LIST_DESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ADDRESS_LIST_DESCRIPTOR, *PADDRESS_LIST_DESCRIPTOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Traffic.h
api_name:
 - ADDRESS_LIST_DESCRIPTOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

