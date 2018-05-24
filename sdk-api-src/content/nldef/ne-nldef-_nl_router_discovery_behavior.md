---
UID: NE:nldef._NL_ROUTER_DISCOVERY_BEHAVIOR
title: "_NL_ROUTER_DISCOVERY_BEHAVIOR"
author: windows-driver-content
description: The NL_ROUTER_DISCOVERY_BEHAVIOR enumeration type defines the router discovery behavior, as described in RFC 2461.
old-location: netvista\nl_router_discovery_behavior.htm
old-project: netvista
ms.assetid: d3a0d872-c90a-4eb5-9011-c5913b9912c6
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: NL_ROUTER_DISCOVERY_BEHAVIOR, NL_ROUTER_DISCOVERY_BEHAVIOR enumeration [Network Drivers Starting with Windows Vista], RouterDiscoveryDhcp, RouterDiscoveryDisabled, RouterDiscoveryEnabled, RouterDiscoveryUnchanged, _NL_ROUTER_DISCOVERY_BEHAVIOR, iphelper_fbaacfeb-efe8-45a1-8cf9-c600ed0214e0.xml, netvista.nl_router_discovery_behavior, nldef/NL_ROUTER_DISCOVERY_BEHAVIOR, nldef/RouterDiscoveryDhcp, nldef/RouterDiscoveryDisabled, nldef/RouterDiscoveryEnabled, nldef/RouterDiscoveryUnchanged
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
req.typenames: NL_ROUTER_DISCOVERY_BEHAVIOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nldef.h
api_name:
-	NL_ROUTER_DISCOVERY_BEHAVIOR
product: Windows
targetos: Windows
req.lib: Newdev.lib
req.dll: Newdev.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _NL_ROUTER_DISCOVERY_BEHAVIOR enumeration


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



