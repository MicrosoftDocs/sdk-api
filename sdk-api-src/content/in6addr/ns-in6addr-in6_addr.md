---
UID: NS:in6addr.in6_addr
title: IN6_ADDR (in6addr.h)
description: The IN6_ADDR structure specifies an IPv6 transport address.
helpviewer_keywords: ["*LPIN6_ADDR","*PIN6_ADDR","IN6_ADDR","IN6_ADDR structure [Network Drivers Starting with Windows Vista]","LPIN6_ADDR","LPIN6_ADDR structure pointer [Network Drivers Starting with Windows Vista]","PIN6_ADDR","PIN6_ADDR structure pointer [Network Drivers Starting with Windows Vista]","in6addr/IN6_ADDR","in6addr/LPIN6_ADDR","in6addr/PIN6_ADDR","netvista.in6_addr","wskref_fd9f043f-fd21-4d2e-b683-0437cf3523c1.xml"]
old-location: netvista\in6_addr.htm
tech.root: NetVista
ms.assetid: 218b07e8-94cf-42f2-a762-13fc1f7c4473
ms.date: 12/05/2018
ms.keywords: '*LPIN6_ADDR, *PIN6_ADDR, IN6_ADDR, IN6_ADDR structure [Network Drivers Starting with Windows Vista], LPIN6_ADDR, LPIN6_ADDR structure pointer [Network Drivers Starting with Windows Vista], PIN6_ADDR, PIN6_ADDR structure pointer [Network Drivers Starting with Windows Vista], in6addr/IN6_ADDR, in6addr/LPIN6_ADDR, in6addr/PIN6_ADDR, netvista.in6_addr, wskref_fd9f043f-fd21-4d2e-b683-0437cf3523c1.xml'
req.header: in6addr.h
req.include-header: Ws2ipdef.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
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
req.typenames: IN6_ADDR, *PIN6_ADDR, *LPIN6_ADDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - in6_addr
 - in6addr/in6_addr
 - PIN6_ADDR
 - in6addr/PIN6_ADDR
 - IN6_ADDR
 - in6addr/IN6_ADDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - in6addr.h
api_name:
 - IN6_ADDR
---

# IN6_ADDR structure


## -description

The IN6_ADDR structure specifies an IPv6 transport address.

## -struct-fields

### -field u

A union that contains the following different representations of the IPv6 transport
     address:

### -field u.Byte

An array that contains 16 UCHAR-typed values.

### -field u.Word

An array that contains eight USHORT-typed values.

## -remarks

All members of the IN6_ADDR structure must be specified in network-byte-order (big-endian).

## -see-also

[SOCKADDR_IN6](../ws2ipdef/ns-ws2ipdef-sockaddr_in6_lh.md)