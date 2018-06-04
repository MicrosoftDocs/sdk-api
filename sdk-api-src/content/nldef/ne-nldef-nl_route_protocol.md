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

# NL_ROUTE_PROTOCOL enumeration


## -description


The NL_ROUTE_PROTOCOL enumeration type defines the routing mechanism that an IP route was added with,
  as described in RFC 4292.


## -enum-fields




### -field RouteProtocolOther

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolLocal

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolNetMgmt

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolIcmp

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolEgp

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolGgp

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolHello

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolRip

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolIsIs

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolEsIs

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolCisco

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolBbn

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolOspf

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolBgp

Reserved for system use. Do not use this value in your driver.


### -field RouteProtocolIdpr


### -field RouteProtocolEigrp


### -field RouteProtocolDvmrp


### -field RouteProtocolRpl


### -field RouteProtocolDhcp




#### - MIB_IPPROTO_BBN

The Bolt, Beranek, and Newman (BBN) Interior Gateway Protocol (IGP) that used the Shortest Path
     First (SPF) algorithm. This protocol was an early dynamic routing protocol.


#### - MIB_IPPROTO_BGP

The Border Gateway Protocol (BGP), a dynamic routing protocol.


#### - MIB_IPPROTO_CISCO

The Cisco Interior Gateway Routing Protocol (IGRP), a dynamic routing protocol.


#### - MIB_IPPROTO_EGP

The Exterior Gateway Protocol (EGP), a dynamic routing protocol.


#### - MIB_IPPROTO_ES_IS

The End System-to-Intermediate System (ES-IS) protocol, a dynamic routing protocol. The ES-IS
     protocol was developed for use in the Open Systems Interconnection (OSI) protocol suite.


#### - MIB_IPPROTO_GGP

The Gateway-to-Gateway Protocol (GGP), a dynamic routing protocol.


#### - MIB_IPPROTO_HELLO

The Hello protocol, a dynamic routing protocol. This value is a historical entry that is no longer
     used and was an early routing protocol that was used by the original ARPANET routers that ran special
     software call fuzzball or hellospeak, as described in RFC 891. For more information, see 
     <a href="http://go.microsoft.com/fwlink/p/?linkid=84070">DCN Local-Network Protocols</a>.


#### - MIB_IPPROTO_ICMP

The result of an ICMP redirect.


#### - MIB_IPPROTO_IS_IS

The Intermediate System-to-Intermediate System (IS-IS) protocol, a dynamic routing protocol. The
     IS-IS protocol was developed for use in the Open Systems Interconnection (OSI) protocol suite.


#### - MIB_IPPROTO_LOCAL

A local interface.


#### - MIB_IPPROTO_NETMGMT

A static route. This value is used to identify route information for IP routing set through
     network management such as the Dynamic Host Configuration Protocol (DCHP) or the Simple Network
     Management Protocol (SNMP), or by calls to the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff546209">CreateIpForwardEntry2</a>, 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff546365">DeleteIpForwardEntry2</a>, or 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff570773">SetIpForwardEntry2</a> functions.


#### - MIB_IPPROTO_NT_AUTOSTATIC

A Windows-specific entry that is added originally by a routing protocol, but which is now
     static.


#### - MIB_IPPROTO_NT_STATIC

A Windows-specific entry that is added as a static route from the routing user interface or a
     routing command.


#### - MIB_IPPROTO_NT_STATIC_NON_DOD

A Windows-specific entry that is added as a static route from the routing user interface or a
     routing command, except that these routes do not cause Dial On Demand (DOD).


#### - MIB_IPPROTO_OSPF

The Open Shortest Path First (OSPF) protocol, a dynamic routing protocol.


#### - MIB_IPPROTO_OTHER

The routing mechanism was not specified.


#### - MIB_IPPROTO_RIP

The Berkeley Routing Information Protocol (RIP) or RIP-II, a dynamic routing protocol.


## -remarks



For more information about RFC 4292, see the 
    <a href="http://go.microsoft.com/fwlink/p/?linkid=84065">IP Forwarding Table MIB</a> memo by the
    Network Working Group.

Note that the 
    Nldef.h header is automatically included by the 
    Netioapi.h header file. Your driver should never use the 
    Nldef.h header file directly.



