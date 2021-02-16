---
UID: NE:adhoc.tagDOT11_ADHOC_NETWORK_CONNECTION_STATUS
title: DOT11_ADHOC_NETWORK_CONNECTION_STATUS (adhoc.h)
description: Specifies the connection state of an ad hoc network.
helpviewer_keywords: ["DOT11_ADHOC_NETWORK_CONNECTION_STATUS","DOT11_ADHOC_NETWORK_CONNECTION_STATUS enumeration [NativeWIFI]","DOT11_ADHOC_NETWORK_CONNECTION_STATUS_CONNECTED","DOT11_ADHOC_NETWORK_CONNECTION_STATUS_CONNECTING","DOT11_ADHOC_NETWORK_CONNECTION_STATUS_DISCONNECTED","DOT11_ADHOC_NETWORK_CONNECTION_STATUS_FORMED","DOT11_ADHOC_NETWORK_CONNECTION_STATUS_INVALID","adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS","adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS_CONNECTED","adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS_CONNECTING","adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS_DISCONNECTED","adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS_FORMED","adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS_INVALID","nwifi.dot11_adhoc_network_connection_status"]
old-location: nwifi\dot11_adhoc_network_connection_status.htm
tech.root: nwifi
ms.assetid: 194179b9-9bd2-4c2f-ab22-c6b95eebfb43
ms.date: 12/05/2018
ms.keywords: DOT11_ADHOC_NETWORK_CONNECTION_STATUS, DOT11_ADHOC_NETWORK_CONNECTION_STATUS enumeration [NativeWIFI], DOT11_ADHOC_NETWORK_CONNECTION_STATUS_CONNECTED, DOT11_ADHOC_NETWORK_CONNECTION_STATUS_CONNECTING, DOT11_ADHOC_NETWORK_CONNECTION_STATUS_DISCONNECTED, DOT11_ADHOC_NETWORK_CONNECTION_STATUS_FORMED, DOT11_ADHOC_NETWORK_CONNECTION_STATUS_INVALID, adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS, adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS_CONNECTED, adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS_CONNECTING, adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS_DISCONNECTED, adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS_FORMED, adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS_INVALID, nwifi.dot11_adhoc_network_connection_status
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDOT11_ADHOC_NETWORK_CONNECTION_STATUS
 - adhoc/tagDOT11_ADHOC_NETWORK_CONNECTION_STATUS
 - DOT11_ADHOC_NETWORK_CONNECTION_STATUS
 - adhoc/DOT11_ADHOC_NETWORK_CONNECTION_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - adhoc.h
api_name:
 - DOT11_ADHOC_NETWORK_CONNECTION_STATUS
---

# DOT11_ADHOC_NETWORK_CONNECTION_STATUS enumeration


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

