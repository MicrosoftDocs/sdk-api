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

# _NET_IF_OPER_STATUS enumeration


## -description


The NET_IF_OPER_STATUS enumeration type defines the current 
  <a href="netvista.ndis_network_interfaces2">NDIS network interface</a> operational
  status.


## -enum-fields




### -field NET_IF_OPER_STATUS_UP

Specifies that the interface is ready to transmit and receive all supported packet types.


### -field NET_IF_OPER_STATUS_DOWN

Specifies that the interface is not ready to transmit or receive data. For example, the media is
     disconnected or the port is not authenticated. In this state, it might be possible to transmit or
     receive some information. For example, if the interface is down because it has not been authenticated,
     802.1<i>x</i> authentication packets can be transmitted and received.


### -field NET_IF_OPER_STATUS_TESTING

Specifies that the interface is in a test mode and no operational packets can be transmitted or
     received.


### -field NET_IF_OPER_STATUS_UNKNOWN

Specifies that the operational status of the network interface cannot be determined.


### -field NET_IF_OPER_STATUS_DORMANT

Specifies that the network interface cannot send or receive packets because the interface is
     waiting for an external event.


### -field NET_IF_OPER_STATUS_NOT_PRESENT

Specifies that the network interface is not ready to transmit or receive data because a component
     is missing in the managed system. This state is more specific than, but similar to, the
     <b>NET_IF_OPER_STATUS_DOWN</b> state.


### -field NET_IF_OPER_STATUS_LOWER_LAYER_DOWN

Specifies that the network interface is not ready to transmit or receive data because underlying
     interfaces are down. This state is more specific than, but similar to, the NET_IF_OPER_STATUS_DOWN
     state.

