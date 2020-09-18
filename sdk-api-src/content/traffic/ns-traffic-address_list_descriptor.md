---
UID: NS:traffic._ADDRESS_LIST_DESCRIPTOR
title: ADDRESS_LIST_DESCRIPTOR (traffic.h)
description: The ADDRESS_LIST_DESCRIPTOR structure provides network address descriptor information for a given interface.
helpviewer_keywords: ["*PADDRESS_LIST_DESCRIPTOR","ADDRESS_LIST_DESCRIPTOR","ADDRESS_LIST_DESCRIPTOR structure [QOS]","PADDRESS_LIST_DESCRIPTOR","PADDRESS_LIST_DESCRIPTOR structure pointer [QOS]","_gqos_address_list_descriptor","qos.address_list_descriptor","traffic/ADDRESS_LIST_DESCRIPTOR","traffic/PADDRESS_LIST_DESCRIPTOR"]
old-location: qos\address_list_descriptor.htm
tech.root: QOS
ms.assetid: d891b82a-999e-4d59-a676-a90648e17699
ms.date: 12/05/2018
ms.keywords: '*PADDRESS_LIST_DESCRIPTOR, ADDRESS_LIST_DESCRIPTOR, ADDRESS_LIST_DESCRIPTOR structure [QOS], PADDRESS_LIST_DESCRIPTOR, PADDRESS_LIST_DESCRIPTOR structure pointer [QOS], _gqos_address_list_descriptor, qos.address_list_descriptor, traffic/ADDRESS_LIST_DESCRIPTOR, traffic/PADDRESS_LIST_DESCRIPTOR'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADDRESS_LIST_DESCRIPTOR, *PADDRESS_LIST_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ADDRESS_LIST_DESCRIPTOR
 - traffic/_ADDRESS_LIST_DESCRIPTOR
 - PADDRESS_LIST_DESCRIPTOR
 - traffic/PADDRESS_LIST_DESCRIPTOR
 - ADDRESS_LIST_DESCRIPTOR
 - traffic/ADDRESS_LIST_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Traffic.h
api_name:
 - ADDRESS_LIST_DESCRIPTOR
---

# ADDRESS_LIST_DESCRIPTOR structure


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

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>