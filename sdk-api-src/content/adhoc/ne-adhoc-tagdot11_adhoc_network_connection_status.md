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

# tagDOT11_ADHOC_NETWORK_CONNECTION_STATUS enumeration


## -description


Specifies the connection state of an ad hoc network.


## -enum-fields




### -field DOT11_ADHOC_NETWORK_CONNECTION_STATUS_INVALID

The connection status cannot be determined. A network with this status should not be used.


### -field DOT11_ADHOC_NETWORK_CONNECTION_STATUS_DISCONNECTED

There are no hosts or clients connected to the network. There are also no pending connection requests for this network.


### -field DOT11_ADHOC_NETWORK_CONNECTION_STATUS_CONNECTING

There is an outstanding connection request. Once the client or host succeeds or fails in its connection attempt, the connection status is updated.


### -field DOT11_ADHOC_NETWORK_CONNECTION_STATUS_CONNECTED

A client or host is connected to the network.


### -field DOT11_ADHOC_NETWORK_CONNECTION_STATUS_FORMED

The network has been formed. Once a client or host connects to the network, the connection status is updated.

