---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# TUNNEL_TYPE enumeration


## -description


The TUNNEL_TYPE enumeration type defines the encapsulation method used by a tunnel, as described by
  the Internet Assigned Names Authority (IANA).


## -enum-fields




### -field TUNNEL_TYPE_NONE

Indicates that a tunnel is not specified.


### -field TUNNEL_TYPE_OTHER

Indicates that none of the following tunnel types is specified.


### -field TUNNEL_TYPE_DIRECT

Specifies that a packet is encapsulated directly within a normal IP header, with no intermediate
     header, and the packet is sent unicast to the remote tunnel endpoint.


### -field TUNNEL_TYPE_6TO4

Specifies that an IPv6 packet is encapsulated directly within an IPv4 header, with no intermediate
     header, and the packet is sent unicast to the destination determined by the 6to4 protocol.


### -field TUNNEL_TYPE_ISATAP

Specifies that an IPv6 packet is encapsulated directly within an IPv4 header, with no intermediate
     header, and the packet is sent unicast to the destination determined by the ISATAP protocol.


### -field TUNNEL_TYPE_TEREDO

Specifies that the tunnel uses Teredo encapsulation.


### -field TUNNEL_TYPE_IPHTTPS

Specifies that the tunnel uses IP over Hypertext Transfer Protocol Secure (HTTPS). This tunnel
     type is supported in Windows 7 and later versions of the Windows operating system.


## -remarks



For more information about the tunnel type as described by the Internet Assigned Names Authority
    (IANA) see 
    <a href="http://go.microsoft.com/fwlink/p/?linkid=60066">"IANAifType-MIB DEFINITIONS"</a>.



