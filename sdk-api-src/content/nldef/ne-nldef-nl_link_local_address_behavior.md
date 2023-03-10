---
UID: NE:nldef._NL_LINK_LOCAL_ADDRESS_BEHAVIOR
title: NL_LINK_LOCAL_ADDRESS_BEHAVIOR (nldef.h)
description: The NL_LINK_LOCAL_ADDRESS_BEHAVIOR enumeration type defines the link local address behavior.
helpviewer_keywords: ["LinkLocalAlwaysOff","LinkLocalAlwaysOn","LinkLocalDelayed","LinkLocalUnchanged","NL_LINK_LOCAL_ADDRESS_BEHAVIOR","NL_LINK_LOCAL_ADDRESS_BEHAVIOR enumeration [Network Drivers Starting with Windows Vista]","iphelper_9f039710-dacb-46b7-b2ff-b7ca7feac810.xml","netvista.nl_link_local_address_behavior","nldef/LinkLocalAlwaysOff","nldef/LinkLocalAlwaysOn","nldef/LinkLocalDelayed","nldef/LinkLocalUnchanged","nldef/NL_LINK_LOCAL_ADDRESS_BEHAVIOR"]
old-location: netvista\nl_link_local_address_behavior.htm
tech.root: NetVista
ms.assetid: d3010b6a-445b-44eb-8ebb-101664f3f835
ms.date: 12/05/2018
ms.keywords: LinkLocalAlwaysOff, LinkLocalAlwaysOn, LinkLocalDelayed, LinkLocalUnchanged, NL_LINK_LOCAL_ADDRESS_BEHAVIOR, NL_LINK_LOCAL_ADDRESS_BEHAVIOR enumeration [Network Drivers Starting with Windows Vista], iphelper_9f039710-dacb-46b7-b2ff-b7ca7feac810.xml, netvista.nl_link_local_address_behavior, nldef/LinkLocalAlwaysOff, nldef/LinkLocalAlwaysOn, nldef/LinkLocalDelayed, nldef/LinkLocalUnchanged, nldef/NL_LINK_LOCAL_ADDRESS_BEHAVIOR
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
targetos: Windows
req.typenames: NL_LINK_LOCAL_ADDRESS_BEHAVIOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NL_LINK_LOCAL_ADDRESS_BEHAVIOR
 - nldef/_NL_LINK_LOCAL_ADDRESS_BEHAVIOR
 - NL_LINK_LOCAL_ADDRESS_BEHAVIOR
 - nldef/NL_LINK_LOCAL_ADDRESS_BEHAVIOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - nldef.h
api_name:
 - NL_LINK_LOCAL_ADDRESS_BEHAVIOR
---

# NL_LINK_LOCAL_ADDRESS_BEHAVIOR enumeration


## -description

The NL_LINK_LOCAL_ADDRESS_BEHAVIOR enumeration type defines the link local address behavior.

## -enum-fields

### -field LinkLocalAlwaysOff:0

A link local IP address should never be used.

### -field LinkLocalDelayed

A link local IP address should be used only if no other address is available. This setting is the
     default setting for an IPv4 interface.

### -field LinkLocalAlwaysOn

A link local IP address should always be used. This setting is the default setting for an IPv6
     interface.

### -field LinkLocalUnchanged:-1

When the properties of an IP interface are being set, the value for link local address behavior
     should be unchanged.

