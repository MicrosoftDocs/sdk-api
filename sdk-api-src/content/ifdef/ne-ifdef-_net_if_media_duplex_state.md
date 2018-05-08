---
UID: NE:ifdef._NET_IF_MEDIA_DUPLEX_STATE
title: "_NET_IF_MEDIA_DUPLEX_STATE"
author: windows-driver-content
description: The NET_IF_MEDIA_DUPLEX_STATE enumeration type specifies the NDIS network interface duplex state.
old-location: netvista\net_if_media_duplex_state.htm
old-project: netvista
ms.assetid: 0bd49b84-0b73-4628-bd86-65b599f791df
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: "*PNET_IF_MEDIA_DUPLEX_STATE, MediaDuplexStateFull, MediaDuplexStateHalf, MediaDuplexStateUnknown, NET_IF_MEDIA_DUPLEX_STATE, NET_IF_MEDIA_DUPLEX_STATE enumeration [Network Drivers Starting with Windows Vista], PNET_IF_MEDIA_DUPLEX_STATE, PNET_IF_MEDIA_DUPLEX_STATE enumeration pointer [Network Drivers Starting with Windows Vista], _NET_IF_MEDIA_DUPLEX_STATE, ifdef/MediaDuplexStateFull, ifdef/MediaDuplexStateHalf, ifdef/MediaDuplexStateUnknown, ifdef/NET_IF_MEDIA_DUPLEX_STATE, ifdef/PNET_IF_MEDIA_DUPLEX_STATE, net_if_enums_ref_b609914b-6556-4d4a-b689-4bd78a995bbd.xml, netvista.net_if_media_duplex_state"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ifdef.h
req.include-header: Netioapi.h, Ntddndis.h
req.target-type: Windows
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
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
req.typenames: NET_IF_MEDIA_DUPLEX_STATE, *PNET_IF_MEDIA_DUPLEX_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ifdef.h
api_name:
-	NET_IF_MEDIA_DUPLEX_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _NET_IF_MEDIA_DUPLEX_STATE enumeration


## -description


The NET_IF_MEDIA_DUPLEX_STATE enumeration type specifies the 
  <a href="netvista.ndis_network_interfaces2">NDIS network interface</a> duplex
  state.


## -enum-fields




### -field MediaDuplexStateUnknown

The duplex state of the miniport adapter is unknown.


### -field MediaDuplexStateHalf

The miniport adapter can transmit or receive but not both simultaneously.


### -field MediaDuplexStateFull

The miniport adapter can transmit and receive simultaneously.


## -remarks



The NDIS_MEDIA_DUPLEX_STATE, enumeration type, used to describe NDIS interface providers in the
    OID_GEN_MEDIA_DUPLEX_STATE, OID, is equivalent to this enumeration.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef NET_IF_MEDIA_DUPLEX_STATE NDIS_MEDIA_DUPLEX_STATE, *PNDIS_MEDIA_DUPLEX_STATE;</pre>
</td>
</tr>
</table></span></div>


