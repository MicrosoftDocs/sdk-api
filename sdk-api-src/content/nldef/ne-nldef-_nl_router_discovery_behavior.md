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



