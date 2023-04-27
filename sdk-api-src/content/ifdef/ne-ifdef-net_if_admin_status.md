---
UID: NE:ifdef._NET_IF_ADMIN_STATUS
title: NET_IF_ADMIN_STATUS (ifdef.h)
description: The NET_IF_ADMIN_STATUS enumeration type specifies the NDIS network interface administrative status, as described in RFC 2863.
helpviewer_keywords: ["*PNET_IF_ADMIN_STATUS","NET_IF_ADMIN_STATUS","NET_IF_ADMIN_STATUS enumeration [Network Drivers Starting with Windows Vista]","NET_IF_ADMIN_STATUS_DOWN","NET_IF_ADMIN_STATUS_TESTING","NET_IF_ADMIN_STATUS_UP","PNET_IF_ADMIN_STATUS","PNET_IF_ADMIN_STATUS enumeration pointer [Network Drivers Starting with Windows Vista]","ifdef/NET_IF_ADMIN_STATUS","ifdef/NET_IF_ADMIN_STATUS_DOWN","ifdef/NET_IF_ADMIN_STATUS_TESTING","ifdef/NET_IF_ADMIN_STATUS_UP","ifdef/PNET_IF_ADMIN_STATUS","net_if_enums_ref_d52428da-7651-4581-8ec4-9409fbfc663f.xml","netvista.net_if_admin_status"]
old-location: netvista\net_if_admin_status.htm
tech.root: NetVista
ms.assetid: 9f6978a9-a779-49c6-b642-c411fa764972
ms.date: 12/05/2018
ms.keywords: '*PNET_IF_ADMIN_STATUS, NET_IF_ADMIN_STATUS, NET_IF_ADMIN_STATUS enumeration [Network Drivers Starting with Windows Vista], NET_IF_ADMIN_STATUS_DOWN, NET_IF_ADMIN_STATUS_TESTING, NET_IF_ADMIN_STATUS_UP, PNET_IF_ADMIN_STATUS, PNET_IF_ADMIN_STATUS enumeration pointer [Network Drivers Starting with Windows Vista], ifdef/NET_IF_ADMIN_STATUS, ifdef/NET_IF_ADMIN_STATUS_DOWN, ifdef/NET_IF_ADMIN_STATUS_TESTING, ifdef/NET_IF_ADMIN_STATUS_UP, ifdef/PNET_IF_ADMIN_STATUS, net_if_enums_ref_d52428da-7651-4581-8ec4-9409fbfc663f.xml, netvista.net_if_admin_status'
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
req.typenames: NET_IF_ADMIN_STATUS, *PNET_IF_ADMIN_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_IF_ADMIN_STATUS
 - ifdef/_NET_IF_ADMIN_STATUS
 - PNET_IF_ADMIN_STATUS
 - ifdef/PNET_IF_ADMIN_STATUS
 - NET_IF_ADMIN_STATUS
 - ifdef/NET_IF_ADMIN_STATUS
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
 - NET_IF_ADMIN_STATUS
---

# NET_IF_ADMIN_STATUS enumeration


## -description

The NET_IF_ADMIN_STATUS enumeration type specifies the 
  <a href="/windows-hardware/drivers/network/ndis-network-interfaces2">NDIS network interface</a> administrative
  status, as described in RFC 2863.

## -enum-fields

### -field NET_IF_ADMIN_STATUS_UP:1

Specifies that the interface is initialized and enabled, but the interface is not necessarily
     ready to transmit and receive network data because that depends on the operational status of the
     interface. For more information about the operational status of an interface, see 
     <a href="/windows-hardware/drivers/network/oid-gen-operational-status">OID_GEN_OPERATIONAL_STATUS</a>.

### -field NET_IF_ADMIN_STATUS_DOWN:2

Specifies that the interface is down, and this interface cannot be used to transmit or receive
     network data.

### -field NET_IF_ADMIN_STATUS_TESTING:3

Specifies that the interface is in a test mode, and no network data can be transmitted or
     received.

## -remarks

For more information on RFC 2863, see 
    <a href="https://www.ietf.org/rfc/rfc2863.txt">"The Interfaces Group MIB"</a>.

## -see-also

<a href="/windows-hardware/drivers/network/oid-gen-admin-status">OID_GEN_ADMIN_STATUS</a>
