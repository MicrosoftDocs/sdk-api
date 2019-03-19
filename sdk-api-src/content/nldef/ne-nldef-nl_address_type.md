---
UID: NE:nldef.__unnamed_enum_4
title: NL_ADDRESS_TYPE (nldef.h)
author: windows-sdk-content
description: The NL_ADDRESS_TYPE enumeration type specifies the IP address type of the network layer.
old-location: netvista\nl_address_type.htm
tech.root: NetVista
ms.assetid: fc91bebc-e023-4f6a-a588-c4f1fbecd200
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PNL_ADDRESS_TYPE, NL_ADDRESS_TYPE, NL_ADDRESS_TYPE enumeration [Network Drivers Starting with Windows Vista], NlatAnycast, NlatBroadcast, NlatInvalid, NlatMulticast, NlatUnicast, NlatUnspecified, PNL_ADDRESS_TYPE, PNL_ADDRESS_TYPE enumeration pointer [Network Drivers Starting with Windows Vista], iphelper_2e71b644-fdff-4c64-bd7f-3f0e24006dc6.xml, netvista.nl_address_type, nldef/NL_ADDRESS_TYPE, nldef/NlatAnycast, nldef/NlatBroadcast, nldef/NlatInvalid, nldef/NlatMulticast, nldef/NlatUnicast, nldef/NlatUnspecified, nldef/PNL_ADDRESS_TYPE"
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
 - NL_ADDRESS_TYPE
product: Windows
targetos: Windows
req.typenames: NL_ADDRESS_TYPE, *PNL_ADDRESS_TYPE
req.redist: 
---

# NL_ADDRESS_TYPE enumeration


## -description


The NL_ADDRESS_TYPE enumeration type specifies the IP address type of the network layer.


## -enum-fields




### -field NlatUnspecified

The unspecified IP address. For example, for IPv4, this address is 0.0.0.0.


### -field NlatUnicast

Any IPv4 or IPv6 unicast address.


### -field NlatAnycast

An IPv6 anycast address.


### -field NlatMulticast

An IPv4 or IPv6 multicast address.


### -field NlatBroadcast

An IPv4 broadcast address.


### -field NlatInvalid

An invalid IP address.

