---
UID: NE:nldef._NL_ROUTER_DISCOVERY_BEHAVIOR
title: NL_ROUTER_DISCOVERY_BEHAVIOR (nldef.h)

description: The NL_ROUTER_DISCOVERY_BEHAVIOR enumeration type defines the router discovery behavior, as described in RFC 2461.
old-location: netvista\nl_router_discovery_behavior.htm
tech.root: NetVista
ms.assetid: d3a0d872-c90a-4eb5-9011-c5913b9912c6

ms.date: 12/05/2018
ms.keywords: NL_ROUTER_DISCOVERY_BEHAVIOR, NL_ROUTER_DISCOVERY_BEHAVIOR enumeration [Network Drivers Starting with Windows Vista], RouterDiscoveryDhcp, RouterDiscoveryDisabled, RouterDiscoveryEnabled, RouterDiscoveryUnchanged, iphelper_fbaacfeb-efe8-45a1-8cf9-c600ed0214e0.xml, netvista.nl_router_discovery_behavior, nldef/NL_ROUTER_DISCOVERY_BEHAVIOR, nldef/RouterDiscoveryDhcp, nldef/RouterDiscoveryDisabled, nldef/RouterDiscoveryEnabled, nldef/RouterDiscoveryUnchanged
ms.topic: enum
f1_keywords: 
 - "nldef/NL_ROUTER_DISCOVERY_BEHAVIOR"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - nldef.h
api_name:
 - NL_ROUTER_DISCOVERY_BEHAVIOR
targetos: Windows
req.typenames: NL_ROUTER_DISCOVERY_BEHAVIOR
req.redist: 
ms.custom: 19H1
---

# NL_ROUTER_DISCOVERY_BEHAVIOR enumeration


## -description


The NL_ROUTER_DISCOVERY_BEHAVIOR enumeration type defines the router discovery behavior, as described
  in RFC 2461.


## -enum-fields




### -field RouterDiscoveryDisabled

Router discovery is disabled.


### -field RouterDiscoveryEnabled

Router discovery is enabled. This setting is the default value for IPv6.


### -field RouterDiscoveryDhcp

Router discovery is configured based on DHCP. This setting is the default value for IPv4.


### -field RouterDiscoveryUnchanged

When the properties of an IP interface are being set, the value for router discovery should be
     unchanged.


## -remarks



For more information about RFC 2461, see the 
    <a href="http://go.microsoft.com/fwlink/p/?linkid=84044">Neighbor Discovery for IP Version 6
    (IPv6)</a> memo by the Network Working Group.



