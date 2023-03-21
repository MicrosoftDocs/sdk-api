---
UID: NE:ifdef._NET_IF_ACCESS_TYPE
title: NET_IF_ACCESS_TYPE (ifdef.h)
description: The NET_IF_ACCESS_TYPE enumeration type specifies the NDIS network interface access type.
helpviewer_keywords: ["*PNET_IF_ACCESS_TYPE","NET_IF_ACCESS_BROADCAST","NET_IF_ACCESS_LOOPBACK","NET_IF_ACCESS_MAXIMUM","NET_IF_ACCESS_POINT_TO_MULTI_POINT","NET_IF_ACCESS_POINT_TO_POINT","NET_IF_ACCESS_TYPE","NET_IF_ACCESS_TYPE enumeration [Network Drivers Starting with Windows Vista]","PNET_IF_ACCESS_TYPE","PNET_IF_ACCESS_TYPE enumeration pointer [Network Drivers Starting with Windows Vista]","ifdef/NET_IF_ACCESS_BROADCAST","ifdef/NET_IF_ACCESS_LOOPBACK","ifdef/NET_IF_ACCESS_MAXIMUM","ifdef/NET_IF_ACCESS_POINT_TO_MULTI_POINT","ifdef/NET_IF_ACCESS_POINT_TO_POINT","ifdef/NET_IF_ACCESS_TYPE","ifdef/PNET_IF_ACCESS_TYPE","net_if_enums_ref_e161dc1a-6445-49e9-ab5b-1e767a78a188.xml","netvista.net_if_access_type"]
old-location: netvista\net_if_access_type.htm
tech.root: NetVista
ms.assetid: 0f8c0866-5ecb-4632-b3bf-cadeee74ce5f
ms.date: 12/05/2018
ms.keywords: '*PNET_IF_ACCESS_TYPE, NET_IF_ACCESS_BROADCAST, NET_IF_ACCESS_LOOPBACK, NET_IF_ACCESS_MAXIMUM, NET_IF_ACCESS_POINT_TO_MULTI_POINT, NET_IF_ACCESS_POINT_TO_POINT, NET_IF_ACCESS_TYPE, NET_IF_ACCESS_TYPE enumeration [Network Drivers Starting with Windows Vista], PNET_IF_ACCESS_TYPE, PNET_IF_ACCESS_TYPE enumeration pointer [Network Drivers Starting with Windows Vista], ifdef/NET_IF_ACCESS_BROADCAST, ifdef/NET_IF_ACCESS_LOOPBACK, ifdef/NET_IF_ACCESS_MAXIMUM, ifdef/NET_IF_ACCESS_POINT_TO_MULTI_POINT, ifdef/NET_IF_ACCESS_POINT_TO_POINT, ifdef/NET_IF_ACCESS_TYPE, ifdef/PNET_IF_ACCESS_TYPE, net_if_enums_ref_e161dc1a-6445-49e9-ab5b-1e767a78a188.xml, netvista.net_if_access_type'
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
req.typenames: NET_IF_ACCESS_TYPE, *PNET_IF_ACCESS_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_IF_ACCESS_TYPE
 - ifdef/_NET_IF_ACCESS_TYPE
 - PNET_IF_ACCESS_TYPE
 - ifdef/PNET_IF_ACCESS_TYPE
 - NET_IF_ACCESS_TYPE
 - ifdef/NET_IF_ACCESS_TYPE
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
 - NET_IF_ACCESS_TYPE
---

# NET_IF_ACCESS_TYPE enumeration


## -description

The NET_IF_ACCESS_TYPE enumeration type specifies the 
  <a href="/windows-hardware/drivers/network/ndis-network-interfaces2">NDIS network interface</a> access
  type.

## -enum-fields

### -field NET_IF_ACCESS_LOOPBACK:1

Specifies the loopback access type. This access type indicates that the interface loops back
     transmit data as receive data.

### -field NET_IF_ACCESS_BROADCAST:2

Specifies the LAN access type, which includes Ethernet. This access type indicates that the
     interface provides native support for multicast or broadcast services.

### -field NET_IF_ACCESS_POINT_TO_POINT:3

Specifies point-to-point access that supports CoNDIS and WAN, except for non-broadcast
     multi-access (NBMA) interfaces.

### -field NET_IF_ACCESS_POINT_TO_MULTI_POINT:4

Specifies point-to-multipoint access that supports non-broadcast multi-access (NBMA) media,
     including the "RAS Internal" interface, and native (non-LANE) ATM.

### -field NET_IF_ACCESS_MAXIMUM:5

A maximum value for testing purposes.
