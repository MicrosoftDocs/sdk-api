---
UID: NE:ifdef.__unnamed_enum_0
title: TUNNEL_TYPE (ifdef.h)
description: The TUNNEL_TYPE enumeration type defines the encapsulation method used by a tunnel, as described by the Internet Assigned Names Authority (IANA).
helpviewer_keywords: ["*PTUNNEL_TYPE","PTUNNEL_TYPE","PTUNNEL_TYPE enumeration pointer [Network Drivers Starting with Windows Vista]","TUNNEL_TYPE","TUNNEL_TYPE enumeration [Network Drivers Starting with Windows Vista]","TUNNEL_TYPE_6TO4","TUNNEL_TYPE_DIRECT","TUNNEL_TYPE_IPHTTPS","TUNNEL_TYPE_ISATAP","TUNNEL_TYPE_NONE","TUNNEL_TYPE_OTHER","TUNNEL_TYPE_TEREDO","ifdef/PTUNNEL_TYPE","ifdef/TUNNEL_TYPE","ifdef/TUNNEL_TYPE_6TO4","ifdef/TUNNEL_TYPE_DIRECT","ifdef/TUNNEL_TYPE_IPHTTPS","ifdef/TUNNEL_TYPE_ISATAP","ifdef/TUNNEL_TYPE_NONE","ifdef/TUNNEL_TYPE_OTHER","ifdef/TUNNEL_TYPE_TEREDO","net_if_enums_ref_46dc254b-c521-4b6e-9780-598bcf1942fa.xml","netvista.tunnel_type"]
old-location: netvista\tunnel_type.htm
tech.root: NetVista
ms.assetid: 3da3701b-9aeb-4e74-b81b-0473fd026d91
ms.date: 12/05/2018
ms.keywords: '*PTUNNEL_TYPE, PTUNNEL_TYPE, PTUNNEL_TYPE enumeration pointer [Network Drivers Starting with Windows Vista], TUNNEL_TYPE, TUNNEL_TYPE enumeration [Network Drivers Starting with Windows Vista], TUNNEL_TYPE_6TO4, TUNNEL_TYPE_DIRECT, TUNNEL_TYPE_IPHTTPS, TUNNEL_TYPE_ISATAP, TUNNEL_TYPE_NONE, TUNNEL_TYPE_OTHER, TUNNEL_TYPE_TEREDO, ifdef/PTUNNEL_TYPE, ifdef/TUNNEL_TYPE, ifdef/TUNNEL_TYPE_6TO4, ifdef/TUNNEL_TYPE_DIRECT, ifdef/TUNNEL_TYPE_IPHTTPS, ifdef/TUNNEL_TYPE_ISATAP, ifdef/TUNNEL_TYPE_NONE, ifdef/TUNNEL_TYPE_OTHER, ifdef/TUNNEL_TYPE_TEREDO, net_if_enums_ref_46dc254b-c521-4b6e-9780-598bcf1942fa.xml, netvista.tunnel_type'
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
req.typenames: TUNNEL_TYPE, *PTUNNEL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PTUNNEL_TYPE
 - ifdef/PTUNNEL_TYPE
 - TUNNEL_TYPE
 - ifdef/TUNNEL_TYPE
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
 - TUNNEL_TYPE
---

# TUNNEL_TYPE enumeration


## -description

The TUNNEL_TYPE enumeration type defines the encapsulation method used by a tunnel, as described by
  the Internet Assigned Names Authority (IANA).

## -enum-fields

### -field TUNNEL_TYPE_NONE:0

Indicates that a tunnel is not specified.

### -field TUNNEL_TYPE_OTHER:1

Indicates that none of the following tunnel types is specified.

### -field TUNNEL_TYPE_DIRECT:2

Specifies that a packet is encapsulated directly within a normal IP header, with no intermediate
     header, and the packet is sent unicast to the remote tunnel endpoint.

### -field TUNNEL_TYPE_6TO4:11

Specifies that an IPv6 packet is encapsulated directly within an IPv4 header, with no intermediate
     header, and the packet is sent unicast to the destination determined by the 6to4 protocol.

### -field TUNNEL_TYPE_ISATAP:13

Specifies that an IPv6 packet is encapsulated directly within an IPv4 header, with no intermediate
     header, and the packet is sent unicast to the destination determined by the ISATAP protocol.

### -field TUNNEL_TYPE_TEREDO:14

Specifies that the tunnel uses Teredo encapsulation.

### -field TUNNEL_TYPE_IPHTTPS:15

Specifies that the tunnel uses IP over Hypertext Transfer Protocol Secure (HTTPS). This tunnel
     type is supported in Windows 7 and later versions of the Windows operating system.

## -remarks

For more information about the tunnel type as described by the Internet Assigned Names Authority
    (IANA) see 
    <a href="https://www.iana.org/assignments/ianaiftype-mib">"IANAifType-MIB DEFINITIONS"</a>.

