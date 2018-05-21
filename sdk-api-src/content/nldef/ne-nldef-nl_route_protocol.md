---
UID: NE:nldef.NL_ROUTE_PROTOCOL
title: NL_ROUTE_PROTOCOL
author: windows-driver-content
description: The NL_ROUTE_PROTOCOL enumeration type defines the routing mechanism that an IP route was added with, as described in RFC 4292.
old-location: netvista\nl_route_protocol.htm
old-project: netvista
ms.assetid: 4bf6256d-e07e-45a8-a269-e32e88642b79
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: "*PNL_ROUTE_PROTOCOL, MIB_IPPROTO_BBN, MIB_IPPROTO_BGP, MIB_IPPROTO_CISCO, MIB_IPPROTO_EGP, MIB_IPPROTO_ES_IS, MIB_IPPROTO_GGP, MIB_IPPROTO_HELLO, MIB_IPPROTO_ICMP, MIB_IPPROTO_IS_IS, MIB_IPPROTO_LOCAL, MIB_IPPROTO_NETMGMT, MIB_IPPROTO_NT_AUTOSTATIC, MIB_IPPROTO_NT_STATIC, MIB_IPPROTO_NT_STATIC_NON_DOD, MIB_IPPROTO_OSPF, MIB_IPPROTO_OTHER, MIB_IPPROTO_RIP, NL_ROUTE_PROTOCOL, NL_ROUTE_PROTOCOL enumeration [Network Drivers Starting with Windows Vista], PNL_ROUTE_PROTOCOL, PNL_ROUTE_PROTOCOL enumeration pointer [Network Drivers Starting with Windows Vista], RouteProtocolBbn, RouteProtocolBgp, RouteProtocolCisco, RouteProtocolEgp, RouteProtocolEsIs, RouteProtocolGgp, RouteProtocolHello, RouteProtocolIcmp, RouteProtocolIsIs, RouteProtocolLocal, RouteProtocolNetMgmt, RouteProtocolOspf, RouteProtocolOther, RouteProtocolRip, iphelper_af0732ae-40e7-4fdf-9ccd-f5c58c4a693b.xml, netvista.nl_route_protocol, nldef/MIB_IPPROTO_BBN, nldef/MIB_IPPROTO_BGP, nldef/MIB_IPPROTO_CISCO, nldef/MIB_IPPROTO_EGP, nldef/MIB_IPPROTO_ES_IS, nldef/MIB_IPPROTO_GGP, nldef/MIB_IPPROTO_HELLO, nldef/MIB_IPPROTO_ICMP, nldef/MIB_IPPROTO_IS_IS, nldef/MIB_IPPROTO_LOCAL, nldef/MIB_IPPROTO_NETMGMT, nldef/MIB_IPPROTO_NT_AUTOSTATIC, nldef/MIB_IPPROTO_NT_STATIC, nldef/MIB_IPPROTO_NT_STATIC_NON_DOD, nldef/MIB_IPPROTO_OSPF, nldef/MIB_IPPROTO_OTHER, nldef/MIB_IPPROTO_RIP, nldef/NL_ROUTE_PROTOCOL, nldef/PNL_ROUTE_PROTOCOL, nldef/RouteProtocolBbn, nldef/RouteProtocolBgp, nldef/RouteProtocolCisco, nldef/RouteProtocolEgp, nldef/RouteProtocolEsIs, nldef/RouteProtocolGgp, nldef/RouteProtocolHello, nldef/RouteProtocolIcmp, nldef/RouteProtocolIsIs, nldef/RouteProtocolLocal, nldef/RouteProtocolNetMgmt, nldef/RouteProtocolOspf, nldef/RouteProtocolOther, nldef/RouteProtocolRip"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: nldef.h
req.include-header: Netioapi.h
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
req.typenames: NL_ROUTE_PROTOCOL, *PNL_ROUTE_PROTOCOL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nldef.h
api_name:
-	NL_ROUTE_PROTOCOL
product: Windows
targetos: Windows
req.lib: Newdev.lib
req.dll: Newdev.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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



