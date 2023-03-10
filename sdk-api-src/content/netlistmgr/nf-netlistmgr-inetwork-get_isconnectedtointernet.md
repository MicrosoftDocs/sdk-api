---
UID: NF:netlistmgr.INetwork.get_IsConnectedToInternet
title: INetwork::get_IsConnectedToInternet (netlistmgr.h)
description: The get_IsConnectedToInternet property specifies if the network has internet connectivity.
helpviewer_keywords: ["INetwork interface [Network Awareness]","get_IsConnectedToInternet method","INetwork.get_IsConnectedToInternet","INetwork::get_IsConnectedToInternet","get_IsConnectedToInternet","get_IsConnectedToInternet method [Network Awareness]","get_IsConnectedToInternet method [Network Awareness]","INetwork interface","netlistmgr/INetwork::get_IsConnectedToInternet","nla.inetwork_get_isconnectedtointernet"]
old-location: nla\inetwork_get_isconnectedtointernet.htm
tech.root: nla
ms.assetid: 12df15aa-64df-426f-aa41-12b96fc35e55
ms.date: 12/05/2018
ms.keywords: INetwork interface [Network Awareness],get_IsConnectedToInternet method, INetwork.get_IsConnectedToInternet, INetwork::get_IsConnectedToInternet, get_IsConnectedToInternet, get_IsConnectedToInternet method [Network Awareness], get_IsConnectedToInternet method [Network Awareness],INetwork interface, netlistmgr/INetwork::get_IsConnectedToInternet, nla.inetwork_get_isconnectedtointernet
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
 - INetwork::get_IsConnectedToInternet
 - netlistmgr/INetwork::get_IsConnectedToInternet
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
 - INetwork.get_IsConnectedToInternet
---

# INetwork::get_IsConnectedToInternet


## -description

The <b>get_IsConnectedToInternet</b> property specifies if the network has internet connectivity.

## -parameters

### -param pbIsConnected [out]

If <b>TRUE</b>, this network has connectivity to the internet; if <b>FALSE</b>, it does not.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a>