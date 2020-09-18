---
UID: NF:netlistmgr.INetworkListManager.get_IsConnectedToInternet
title: INetworkListManager::get_IsConnectedToInternet (netlistmgr.h)
description: The get_IsConnectedToInternet property specifies if the local machine has internet connectivity.
helpviewer_keywords: ["INetworkListManager interface [Network Awareness]","get_IsConnectedToInternet method","INetworkListManager.get_IsConnectedToInternet","INetworkListManager::get_IsConnectedToInternet","get_IsConnectedToInternet","get_IsConnectedToInternet method [Network Awareness]","get_IsConnectedToInternet method [Network Awareness]","INetworkListManager interface","netlistmgr/INetworkListManager::get_IsConnectedToInternet","nla.inetworklistmanager_get_isconnectedtointernet"]
old-location: nla\inetworklistmanager_get_isconnectedtointernet.htm
tech.root: nla
ms.assetid: b3f06da5-c0e2-4c56-87af-b180aa87c827
ms.date: 12/05/2018
ms.keywords: INetworkListManager interface [Network Awareness],get_IsConnectedToInternet method, INetworkListManager.get_IsConnectedToInternet, INetworkListManager::get_IsConnectedToInternet, get_IsConnectedToInternet, get_IsConnectedToInternet method [Network Awareness], get_IsConnectedToInternet method [Network Awareness],INetworkListManager interface, netlistmgr/INetworkListManager::get_IsConnectedToInternet, nla.inetworklistmanager_get_isconnectedtointernet
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
 - INetworkListManager::get_IsConnectedToInternet
 - netlistmgr/INetworkListManager::get_IsConnectedToInternet
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
 - INetworkListManager.get_IsConnectedToInternet
---

# INetworkListManager::get_IsConnectedToInternet


## -description

The <b>get_IsConnectedToInternet</b> property specifies if the local machine has internet connectivity.

## -parameters

### -param pbIsConnected [out]

If <b>TRUE</b>, the local machine is connected to the internet; if <b>FALSE</b>, it is not.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworklistmanager">INetworkListManager</a>