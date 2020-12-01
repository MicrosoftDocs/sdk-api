---
UID: NE:ifdef._NET_IF_MEDIA_DUPLEX_STATE
title: NET_IF_MEDIA_DUPLEX_STATE (ifdef.h)
description: The NET_IF_MEDIA_DUPLEX_STATE enumeration type specifies the NDIS network interface duplex state.
helpviewer_keywords: ["*PNET_IF_MEDIA_DUPLEX_STATE","MediaDuplexStateFull","MediaDuplexStateHalf","MediaDuplexStateUnknown","NET_IF_MEDIA_DUPLEX_STATE","NET_IF_MEDIA_DUPLEX_STATE enumeration [Network Drivers Starting with Windows Vista]","PNET_IF_MEDIA_DUPLEX_STATE","PNET_IF_MEDIA_DUPLEX_STATE enumeration pointer [Network Drivers Starting with Windows Vista]","ifdef/MediaDuplexStateFull","ifdef/MediaDuplexStateHalf","ifdef/MediaDuplexStateUnknown","ifdef/NET_IF_MEDIA_DUPLEX_STATE","ifdef/PNET_IF_MEDIA_DUPLEX_STATE","net_if_enums_ref_b609914b-6556-4d4a-b689-4bd78a995bbd.xml","netvista.net_if_media_duplex_state"]
old-location: netvista\net_if_media_duplex_state.htm
tech.root: NetVista
ms.assetid: 0bd49b84-0b73-4628-bd86-65b599f791df
ms.date: 12/05/2018
ms.keywords: '*PNET_IF_MEDIA_DUPLEX_STATE, MediaDuplexStateFull, MediaDuplexStateHalf, MediaDuplexStateUnknown, NET_IF_MEDIA_DUPLEX_STATE, NET_IF_MEDIA_DUPLEX_STATE enumeration [Network Drivers Starting with Windows Vista], PNET_IF_MEDIA_DUPLEX_STATE, PNET_IF_MEDIA_DUPLEX_STATE enumeration pointer [Network Drivers Starting with Windows Vista], ifdef/MediaDuplexStateFull, ifdef/MediaDuplexStateHalf, ifdef/MediaDuplexStateUnknown, ifdef/NET_IF_MEDIA_DUPLEX_STATE, ifdef/PNET_IF_MEDIA_DUPLEX_STATE, net_if_enums_ref_b609914b-6556-4d4a-b689-4bd78a995bbd.xml, netvista.net_if_media_duplex_state'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NET_IF_MEDIA_DUPLEX_STATE, *PNET_IF_MEDIA_DUPLEX_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_IF_MEDIA_DUPLEX_STATE
 - ifdef/_NET_IF_MEDIA_DUPLEX_STATE
 - PNET_IF_MEDIA_DUPLEX_STATE
 - ifdef/PNET_IF_MEDIA_DUPLEX_STATE
 - NET_IF_MEDIA_DUPLEX_STATE
 - ifdef/NET_IF_MEDIA_DUPLEX_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ifdef.h
api_name:
 - NET_IF_MEDIA_DUPLEX_STATE
---

# NET_IF_MEDIA_DUPLEX_STATE enumeration


## -description

The NET_IF_MEDIA_DUPLEX_STATE enumeration type specifies the 
  <a href="/windows-hardware/drivers/network/ndis-network-interfaces2">NDIS network interface</a> duplex
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


```
typedef NET_IF_MEDIA_DUPLEX_STATE NDIS_MEDIA_DUPLEX_STATE, *PNDIS_MEDIA_DUPLEX_STATE;
```