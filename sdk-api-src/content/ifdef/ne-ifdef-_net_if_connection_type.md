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

# _NET_IF_CONNECTION_TYPE enumeration


## -description


The NET_IF_CONNECTION_TYPE enumeration type specifies the 
  <a href="netvista.ndis_network_interfaces2">NDIS network interface</a> connection
  type.


## -enum-fields




### -field NET_IF_CONNECTION_DEDICATED

Specifies the dedicated connection type. The connection comes up automatically when media sense is
     <b>TRUE</b>. For example, an Ethernet connection is dedicated.


### -field NET_IF_CONNECTION_PASSIVE

Specifies the passive connection type. The other end must bring up the connection to the local
     station. For example, the RAS interface is passive.


### -field NET_IF_CONNECTION_DEMAND

Specifies the demand-dial connection type. A demand-dial connection comes up in response to a
     local action--for example, sending a packet.


### -field NET_IF_CONNECTION_MAXIMUM

A maximum value for testing purposes.

