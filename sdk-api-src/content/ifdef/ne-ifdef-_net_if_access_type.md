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

# _NET_IF_ACCESS_TYPE enumeration


## -description


The NET_IF_ACCESS_TYPE enumeration type specifies the 
  <a href="netvista.ndis_network_interfaces2">NDIS network interface</a> access
  type.


## -enum-fields




### -field NET_IF_ACCESS_LOOPBACK

Specifies the loopback access type. This access type indicates that the interface loops back
     transmit data as receive data.


### -field NET_IF_ACCESS_BROADCAST

Specifies the LAN access type, which includes Ethernet. This access type indicates that the
     interface provides native support for multicast or broadcast services.


### -field NET_IF_ACCESS_POINT_TO_POINT

Specifies point-to-point access that supports CoNDIS and WAN, except for non-broadcast
     multi-access (NBMA) interfaces.


### -field NET_IF_ACCESS_POINT_TO_MULTI_POINT

Specifies point-to-multipoint access that supports non-broadcast multi-access (NBMA) media,
     including the "RAS Internal" interface, and native (non-LANE) ATM.


### -field NET_IF_ACCESS_MAXIMUM

A maximum value for testing purposes.

