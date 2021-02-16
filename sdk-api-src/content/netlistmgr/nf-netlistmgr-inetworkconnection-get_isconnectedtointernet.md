---
UID: NF:netlistmgr.INetworkConnection.get_IsConnectedToInternet
title: INetworkConnection::get_IsConnectedToInternet (netlistmgr.h)
description: The get_IsConnectedToInternet property specifies if the associated network connection has internet connectivity.
helpviewer_keywords: ["INetworkConnection interface [Network Awareness]","get_IsConnectedToInternet method","INetworkConnection.get_IsConnectedToInternet","INetworkConnection::get_IsConnectedToInternet","get_IsConnectedToInternet","get_IsConnectedToInternet method [Network Awareness]","get_IsConnectedToInternet method [Network Awareness]","INetworkConnection interface","netlistmgr/INetworkConnection::get_IsConnectedToInternet","nla.inetworkconnection_get_isconnectedtointernet"]
old-location: nla\inetworkconnection_get_isconnectedtointernet.htm
tech.root: nla
ms.assetid: c5ac2d6b-c96a-478f-add3-617c544dfaf0
ms.date: 12/05/2018
ms.keywords: INetworkConnection interface [Network Awareness],get_IsConnectedToInternet method, INetworkConnection.get_IsConnectedToInternet, INetworkConnection::get_IsConnectedToInternet, get_IsConnectedToInternet, get_IsConnectedToInternet method [Network Awareness], get_IsConnectedToInternet method [Network Awareness],INetworkConnection interface, netlistmgr/INetworkConnection::get_IsConnectedToInternet, nla.inetworkconnection_get_isconnectedtointernet
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
 - INetworkConnection::get_IsConnectedToInternet
 - netlistmgr/INetworkConnection::get_IsConnectedToInternet
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
 - INetworkConnection.get_IsConnectedToInternet
---

# INetworkConnection::get_IsConnectedToInternet


## -description

The get_IsConnectedToInternet property specifies if the associated network connection has internet connectivity.

## -parameters

### -param pbIsConnected [out]

If <b>TRUE</b>, this network connection has connectivity to the internet; if <b>FALSE</b>, it does not.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a>