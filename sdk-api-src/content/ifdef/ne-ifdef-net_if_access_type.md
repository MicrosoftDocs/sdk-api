---
UID: NE:ifdef._NET_IF_ACCESS_TYPE
title: NET_IF_ACCESS_TYPE
author: windows-sdk-content
description: The NET_IF_ACCESS_TYPE enumeration type specifies the NDIS network interface access type.
old-location: netvista\net_if_access_type.htm
tech.root: NetVista
ms.assetid: 0f8c0866-5ecb-4632-b3bf-cadeee74ce5f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PNET_IF_ACCESS_TYPE, NET_IF_ACCESS_BROADCAST, NET_IF_ACCESS_LOOPBACK, NET_IF_ACCESS_MAXIMUM, NET_IF_ACCESS_POINT_TO_MULTI_POINT, NET_IF_ACCESS_POINT_TO_POINT, NET_IF_ACCESS_TYPE, NET_IF_ACCESS_TYPE enumeration [Network Drivers Starting with Windows Vista], PNET_IF_ACCESS_TYPE, PNET_IF_ACCESS_TYPE enumeration pointer [Network Drivers Starting with Windows Vista], ifdef/NET_IF_ACCESS_BROADCAST, ifdef/NET_IF_ACCESS_LOOPBACK, ifdef/NET_IF_ACCESS_MAXIMUM, ifdef/NET_IF_ACCESS_POINT_TO_MULTI_POINT, ifdef/NET_IF_ACCESS_POINT_TO_POINT, ifdef/NET_IF_ACCESS_TYPE, ifdef/PNET_IF_ACCESS_TYPE, net_if_enums_ref_e161dc1a-6445-49e9-ab5b-1e767a78a188.xml, netvista.net_if_access_type"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ifdef.h
api_name:
 - NET_IF_ACCESS_TYPE
product: Windows
targetos: Windows
req.typenames: NET_IF_ACCESS_TYPE, *PNET_IF_ACCESS_TYPE
req.redist: 
---

# NET_IF_ACCESS_TYPE enumeration


## -description


The NET_IF_ACCESS_TYPE enumeration type specifies the 
  <a href="netvista.ndis_network_interfaces2">NDIS network interface</a> access
  type.


## -enum-fields




### -field NET_IF_ACCESS_LOOPBACK

Specifies the loopback access type. This access type indicates that the interface loops back
     transmit data as receive data.


### -field NET_IF_ACCESS_BROADCAST

Specifies the LAN access type, which includes Ethernet. This access type indicates that the
     interface provides native support for multicast or broadcast services.


### -field NET_IF_ACCESS_POINT_TO_POINT

Specifies point-to-point access that supports CoNDIS and WAN, except for non-broadcast
     multi-access (NBMA) interfaces.


### -field NET_IF_ACCESS_POINT_TO_MULTI_POINT

Specifies point-to-multipoint access that supports non-broadcast multi-access (NBMA) media,
     including the "RAS Internal" interface, and native (non-LANE) ATM.


### -field NET_IF_ACCESS_MAXIMUM

A maximum value for testing purposes.

