---
UID: NE:ifdef._NET_IF_DIRECTION_TYPE
title: NET_IF_DIRECTION_TYPE
author: windows-sdk-content
description: The NET_IF_ACCESS_TYPE enumeration type specifies the NDIS network interface direction type.
old-location: netvista\net_if_direction_type.htm
tech.root: NetVista
ms.assetid: e9f80162-5a1c-44c8-af31-a0c0f986edc2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PNET_IF_DIRECTION_TYPE, NET_IF_DIRECTION_MAXIMUM, NET_IF_DIRECTION_RECEIVEONLY, NET_IF_DIRECTION_SENDONLY, NET_IF_DIRECTION_SENDRECEIVE, NET_IF_DIRECTION_TYPE, NET_IF_DIRECTION_TYPE enumeration [Network Drivers Starting with Windows Vista], PNET_IF_DIRECTION_TYPE, PNET_IF_DIRECTION_TYPE enumeration pointer [Network Drivers Starting with Windows Vista], ifdef/NET_IF_DIRECTION_MAXIMUM, ifdef/NET_IF_DIRECTION_RECEIVEONLY, ifdef/NET_IF_DIRECTION_SENDONLY, ifdef/NET_IF_DIRECTION_SENDRECEIVE, ifdef/NET_IF_DIRECTION_TYPE, ifdef/PNET_IF_DIRECTION_TYPE, net_if_enums_ref_a000a0bc-2ed9-4d45-af32-4cfb71731367.xml, netvista.net_if_direction_type"
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
 - NET_IF_DIRECTION_TYPE
product: Windows
targetos: Windows
req.typenames: NET_IF_DIRECTION_TYPE, *PNET_IF_DIRECTION_TYPE
req.redist: 
---

# NET_IF_DIRECTION_TYPE enumeration


## -description


The NET_IF_ACCESS_TYPE enumeration type specifies the 
  <a href="https://msdn.microsoft.com/library/Ff566527(v=VS.85).aspx">NDIS network interface</a> direction
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

