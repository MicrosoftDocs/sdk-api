---
UID: NF:netlistmgr.INetworkListManager.get_IsConnected
title: INetworkListManager::get_IsConnected (netlistmgr.h)
description: The get_IsConnected property specifies if the local machine has network connectivity.
helpviewer_keywords: ["INetworkListManager interface [Network Awareness]","get_IsConnected method","INetworkListManager.get_IsConnected","INetworkListManager::get_IsConnected","get_IsConnected","get_IsConnected method [Network Awareness]","get_IsConnected method [Network Awareness]","INetworkListManager interface","netlistmgr/INetworkListManager::get_IsConnected","nla.inetworklistmanager_get_isconnected"]
old-location: nla\inetworklistmanager_get_isconnected.htm
tech.root: nla
ms.assetid: 51bdec8e-521f-4673-a2ad-07e8995f3905
ms.date: 12/05/2018
ms.keywords: INetworkListManager interface [Network Awareness],get_IsConnected method, INetworkListManager.get_IsConnected, INetworkListManager::get_IsConnected, get_IsConnected, get_IsConnected method [Network Awareness], get_IsConnected method [Network Awareness],INetworkListManager interface, netlistmgr/INetworkListManager::get_IsConnected, nla.inetworklistmanager_get_isconnected
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
 - INetworkListManager::get_IsConnected
 - netlistmgr/INetworkListManager::get_IsConnected
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
 - INetworkListManager.get_IsConnected
---

# INetworkListManager::get_IsConnected


## -description

The <b>get_IsConnected</b> property specifies if the local machine has network connectivity.

## -parameters

### -param pbIsConnected [out]

If <b>TRUE</b> ,  the network has at least local connectivity via ipv4 or ipv6 or both. The network may also have internet connectivity.  Thus, the network is connected.

If <b>FALSE</b>, the network does not have local or internet connectivity. The network is not connected.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a>