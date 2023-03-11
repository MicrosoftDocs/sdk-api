---
UID: NE:ifdef._NET_IF_OPER_STATUS
title: NET_IF_OPER_STATUS (ifdef.h)
description: The NET_IF_OPER_STATUS enumeration type defines the current NDIS network interface operational status.
helpviewer_keywords: ["*PNET_IF_OPER_STATUS","NET_IF_OPER_STATUS","NET_IF_OPER_STATUS enumeration [Network Drivers Starting with Windows Vista]","NET_IF_OPER_STATUS_DORMANT","NET_IF_OPER_STATUS_DOWN","NET_IF_OPER_STATUS_LOWER_LAYER_DOWN","NET_IF_OPER_STATUS_NOT_PRESENT","NET_IF_OPER_STATUS_TESTING","NET_IF_OPER_STATUS_UNKNOWN","NET_IF_OPER_STATUS_UP","PNET_IF_OPER_STATUS","PNET_IF_OPER_STATUS enumeration pointer [Network Drivers Starting with Windows Vista]","ifdef/NET_IF_OPER_STATUS","ifdef/NET_IF_OPER_STATUS_DORMANT","ifdef/NET_IF_OPER_STATUS_DOWN","ifdef/NET_IF_OPER_STATUS_LOWER_LAYER_DOWN","ifdef/NET_IF_OPER_STATUS_NOT_PRESENT","ifdef/NET_IF_OPER_STATUS_TESTING","ifdef/NET_IF_OPER_STATUS_UNKNOWN","ifdef/NET_IF_OPER_STATUS_UP","ifdef/PNET_IF_OPER_STATUS","net_if_enums_ref_c9b9e5f0-12cc-4499-8d9a-e40b088470b8.xml","netvista.net_if_oper_status"]
old-location: netvista\net_if_oper_status.htm
tech.root: NetVista
ms.assetid: 19bd5b9b-94db-430e-b264-1744dfe83d54
ms.date: 12/05/2018
ms.keywords: '*PNET_IF_OPER_STATUS, NET_IF_OPER_STATUS, NET_IF_OPER_STATUS enumeration [Network Drivers Starting with Windows Vista], NET_IF_OPER_STATUS_DORMANT, NET_IF_OPER_STATUS_DOWN, NET_IF_OPER_STATUS_LOWER_LAYER_DOWN, NET_IF_OPER_STATUS_NOT_PRESENT, NET_IF_OPER_STATUS_TESTING, NET_IF_OPER_STATUS_UNKNOWN, NET_IF_OPER_STATUS_UP, PNET_IF_OPER_STATUS, PNET_IF_OPER_STATUS enumeration pointer [Network Drivers Starting with Windows Vista], ifdef/NET_IF_OPER_STATUS, ifdef/NET_IF_OPER_STATUS_DORMANT, ifdef/NET_IF_OPER_STATUS_DOWN, ifdef/NET_IF_OPER_STATUS_LOWER_LAYER_DOWN, ifdef/NET_IF_OPER_STATUS_NOT_PRESENT, ifdef/NET_IF_OPER_STATUS_TESTING, ifdef/NET_IF_OPER_STATUS_UNKNOWN, ifdef/NET_IF_OPER_STATUS_UP, ifdef/PNET_IF_OPER_STATUS, net_if_enums_ref_c9b9e5f0-12cc-4499-8d9a-e40b088470b8.xml, netvista.net_if_oper_status'
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
req.typenames: NET_IF_OPER_STATUS, *PNET_IF_OPER_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_IF_OPER_STATUS
 - ifdef/_NET_IF_OPER_STATUS
 - PNET_IF_OPER_STATUS
 - ifdef/PNET_IF_OPER_STATUS
 - NET_IF_OPER_STATUS
 - ifdef/NET_IF_OPER_STATUS
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
 - NET_IF_OPER_STATUS
---

# NET_IF_OPER_STATUS enumeration


## -description

The NET_IF_OPER_STATUS enumeration type defines the current 
  <a href="/windows-hardware/drivers/network/ndis-network-interfaces2">NDIS network interface</a> operational
  status.

## -enum-fields

### -field NET_IF_OPER_STATUS_UP:1

Specifies that the interface is ready to transmit and receive all supported packet types.

### -field NET_IF_OPER_STATUS_DOWN:2

Specifies that the interface is not ready to transmit or receive data. For example, the media is
     disconnected or the port is not authenticated. In this state, it might be possible to transmit or
     receive some information. For example, if the interface is down because it has not been authenticated,
     802.1<i>x</i> authentication packets can be transmitted and received.

### -field NET_IF_OPER_STATUS_TESTING:3

Specifies that the interface is in a test mode and no operational packets can be transmitted or
     received.

### -field NET_IF_OPER_STATUS_UNKNOWN:4

Specifies that the operational status of the network interface cannot be determined.

### -field NET_IF_OPER_STATUS_DORMANT:5

Specifies that the network interface cannot send or receive packets because the interface is
     waiting for an external event.

### -field NET_IF_OPER_STATUS_NOT_PRESENT:6

Specifies that the network interface is not ready to transmit or receive data because a component
     is missing in the managed system. This state is more specific than, but similar to, the
     <b>NET_IF_OPER_STATUS_DOWN</b> state.

### -field NET_IF_OPER_STATUS_LOWER_LAYER_DOWN:7

Specifies that the network interface is not ready to transmit or receive data because underlying
     interfaces are down. This state is more specific than, but similar to, the NET_IF_OPER_STATUS_DOWN
     state.
