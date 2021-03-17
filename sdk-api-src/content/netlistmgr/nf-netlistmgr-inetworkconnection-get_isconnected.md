---
UID: NF:netlistmgr.INetworkConnection.get_IsConnected
title: INetworkConnection::get_IsConnected (netlistmgr.h)
description: The get_IsConnected property specifies if the associated network connection has network connectivity.
helpviewer_keywords: ["INetworkConnection interface [Network Awareness]","get_IsConnected method","INetworkConnection.get_IsConnected","INetworkConnection::get_IsConnected","get_IsConnected","get_IsConnected method [Network Awareness]","get_IsConnected method [Network Awareness]","INetworkConnection interface","netlistmgr/INetworkConnection::get_IsConnected","nla.inetworkconnection_get_isconnected"]
old-location: nla\inetworkconnection_get_isconnected.htm
tech.root: nla
ms.assetid: bf5a8997-306a-47fe-8e2b-ad9b3efe14db
ms.date: 12/05/2018
ms.keywords: INetworkConnection interface [Network Awareness],get_IsConnected method, INetworkConnection.get_IsConnected, INetworkConnection::get_IsConnected, get_IsConnected, get_IsConnected method [Network Awareness], get_IsConnected method [Network Awareness],INetworkConnection interface, netlistmgr/INetworkConnection::get_IsConnected, nla.inetworkconnection_get_isconnected
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetworkConnection::get_IsConnected
 - netlistmgr/INetworkConnection::get_IsConnected
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Netlistmgr.h
api_name:
 - INetworkConnection.get_IsConnected
---

# INetworkConnection::get_IsConnected


## -description

The <b>get_IsConnected</b> property specifies if the associated network connection has network connectivity.

## -parameters

### -param pbIsConnected [out]

If <b>TRUE</b>, this network connection has connectivity; if <b>FALSE</b>, it does not.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a>