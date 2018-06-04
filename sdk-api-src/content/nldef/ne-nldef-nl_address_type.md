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

