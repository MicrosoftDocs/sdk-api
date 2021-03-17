---
UID: NE:ifdef._NET_IF_DIRECTION_TYPE
title: NET_IF_DIRECTION_TYPE (ifdef.h)
description: The NET_IF_ACCESS_TYPE enumeration type specifies the NDIS network interface direction type.
helpviewer_keywords: ["*PNET_IF_DIRECTION_TYPE","NET_IF_DIRECTION_MAXIMUM","NET_IF_DIRECTION_RECEIVEONLY","NET_IF_DIRECTION_SENDONLY","NET_IF_DIRECTION_SENDRECEIVE","NET_IF_DIRECTION_TYPE","NET_IF_DIRECTION_TYPE enumeration [Network Drivers Starting with Windows Vista]","PNET_IF_DIRECTION_TYPE","PNET_IF_DIRECTION_TYPE enumeration pointer [Network Drivers Starting with Windows Vista]","ifdef/NET_IF_DIRECTION_MAXIMUM","ifdef/NET_IF_DIRECTION_RECEIVEONLY","ifdef/NET_IF_DIRECTION_SENDONLY","ifdef/NET_IF_DIRECTION_SENDRECEIVE","ifdef/NET_IF_DIRECTION_TYPE","ifdef/PNET_IF_DIRECTION_TYPE","net_if_enums_ref_a000a0bc-2ed9-4d45-af32-4cfb71731367.xml","netvista.net_if_direction_type"]
old-location: netvista\net_if_direction_type.htm
tech.root: NetVista
ms.assetid: e9f80162-5a1c-44c8-af31-a0c0f986edc2
ms.date: 12/05/2018
ms.keywords: '*PNET_IF_DIRECTION_TYPE, NET_IF_DIRECTION_MAXIMUM, NET_IF_DIRECTION_RECEIVEONLY, NET_IF_DIRECTION_SENDONLY, NET_IF_DIRECTION_SENDRECEIVE, NET_IF_DIRECTION_TYPE, NET_IF_DIRECTION_TYPE enumeration [Network Drivers Starting with Windows Vista], PNET_IF_DIRECTION_TYPE, PNET_IF_DIRECTION_TYPE enumeration pointer [Network Drivers Starting with Windows Vista], ifdef/NET_IF_DIRECTION_MAXIMUM, ifdef/NET_IF_DIRECTION_RECEIVEONLY, ifdef/NET_IF_DIRECTION_SENDONLY, ifdef/NET_IF_DIRECTION_SENDRECEIVE, ifdef/NET_IF_DIRECTION_TYPE, ifdef/PNET_IF_DIRECTION_TYPE, net_if_enums_ref_a000a0bc-2ed9-4d45-af32-4cfb71731367.xml, netvista.net_if_direction_type'
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
req.typenames: NET_IF_DIRECTION_TYPE, *PNET_IF_DIRECTION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_IF_DIRECTION_TYPE
 - ifdef/_NET_IF_DIRECTION_TYPE
 - PNET_IF_DIRECTION_TYPE
 - ifdef/PNET_IF_DIRECTION_TYPE
 - NET_IF_DIRECTION_TYPE
 - ifdef/NET_IF_DIRECTION_TYPE
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
 - NET_IF_DIRECTION_TYPE
---

# NET_IF_DIRECTION_TYPE enumeration


## -description

The NET_IF_ACCESS_TYPE enumeration type specifies the 
  <a href="/windows-hardware/drivers/network/ndis-network-interfaces2">NDIS network interface</a> direction
  type.

## -enum-fields

### -field NET_IF_DIRECTION_SENDRECEIVE

Indicates the send and receive direction type. This direction type indicates that the NDIS network
     interface can send and receive data.

### -field NET_IF_DIRECTION_SENDONLY

Indicates the send only direction type. This direction type indicates that the NDIS network
     interface can only send data.

### -field NET_IF_DIRECTION_RECEIVEONLY

Indicates the receive only direction type. This direction type indicates that the NDIS network
     interface can only receive data.

### -field NET_IF_DIRECTION_MAXIMUM

A maximum value for testing purposes.