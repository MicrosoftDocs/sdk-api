---
UID: NE:ifdef._NET_IF_CONNECTION_TYPE
title: NET_IF_CONNECTION_TYPE (ifdef.h)
description: The NET_IF_CONNECTION_TYPE enumeration type specifies the NDIS network interface connection type.
helpviewer_keywords: ["*PNET_IF_CONNECTION_TYPE","NET_IF_CONNECTION_DEDICATED","NET_IF_CONNECTION_DEMAND","NET_IF_CONNECTION_MAXIMUM","NET_IF_CONNECTION_PASSIVE","NET_IF_CONNECTION_TYPE","NET_IF_CONNECTION_TYPE enumeration [Network Drivers Starting with Windows Vista]","PNET_IF_CONNECTION_TYPE","PNET_IF_CONNECTION_TYPE enumeration pointer [Network Drivers Starting with Windows Vista]","ifdef/NET_IF_CONNECTION_DEDICATED","ifdef/NET_IF_CONNECTION_DEMAND","ifdef/NET_IF_CONNECTION_MAXIMUM","ifdef/NET_IF_CONNECTION_PASSIVE","ifdef/NET_IF_CONNECTION_TYPE","ifdef/PNET_IF_CONNECTION_TYPE","net_if_enums_ref_b37dfff6-f81c-4633-a409-82535736247b.xml","netvista.net_if_connection_type"]
old-location: netvista\net_if_connection_type.htm
tech.root: NetVista
ms.assetid: af1ffcf2-65cf-4d80-b702-a843b6d19fdc
ms.date: 12/05/2018
ms.keywords: '*PNET_IF_CONNECTION_TYPE, NET_IF_CONNECTION_DEDICATED, NET_IF_CONNECTION_DEMAND, NET_IF_CONNECTION_MAXIMUM, NET_IF_CONNECTION_PASSIVE, NET_IF_CONNECTION_TYPE, NET_IF_CONNECTION_TYPE enumeration [Network Drivers Starting with Windows Vista], PNET_IF_CONNECTION_TYPE, PNET_IF_CONNECTION_TYPE enumeration pointer [Network Drivers Starting with Windows Vista], ifdef/NET_IF_CONNECTION_DEDICATED, ifdef/NET_IF_CONNECTION_DEMAND, ifdef/NET_IF_CONNECTION_MAXIMUM, ifdef/NET_IF_CONNECTION_PASSIVE, ifdef/NET_IF_CONNECTION_TYPE, ifdef/PNET_IF_CONNECTION_TYPE, net_if_enums_ref_b37dfff6-f81c-4633-a409-82535736247b.xml, netvista.net_if_connection_type'
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
req.typenames: NET_IF_CONNECTION_TYPE, *PNET_IF_CONNECTION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_IF_CONNECTION_TYPE
 - ifdef/_NET_IF_CONNECTION_TYPE
 - PNET_IF_CONNECTION_TYPE
 - ifdef/PNET_IF_CONNECTION_TYPE
 - NET_IF_CONNECTION_TYPE
 - ifdef/NET_IF_CONNECTION_TYPE
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
 - NET_IF_CONNECTION_TYPE
---

# NET_IF_CONNECTION_TYPE enumeration


## -description

The NET_IF_CONNECTION_TYPE enumeration type specifies the 
  <a href="/windows-hardware/drivers/network/ndis-network-interfaces2">NDIS network interface</a> connection
  type.

## -enum-fields

### -field NET_IF_CONNECTION_DEDICATED:1

Specifies the dedicated connection type. The connection comes up automatically when media sense is
     <b>TRUE</b>. For example, an Ethernet connection is dedicated.

### -field NET_IF_CONNECTION_PASSIVE:2

Specifies the passive connection type. The other end must bring up the connection to the local
     station. For example, the RAS interface is passive.

### -field NET_IF_CONNECTION_DEMAND:3

Specifies the demand-dial connection type. A demand-dial connection comes up in response to a
     local action--for example, sending a packet.

### -field NET_IF_CONNECTION_MAXIMUM:4

A maximum value for testing purposes.
