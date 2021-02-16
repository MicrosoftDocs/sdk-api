---
UID: NF:netlistmgr.INetwork.GetNetworkConnections
title: INetwork::GetNetworkConnections (netlistmgr.h)
description: The GetNetworkConnections method returns an enumeration of all network connections for a network. A network can have multiple connections to it from different interfaces or different links from the same interface.
helpviewer_keywords: ["GetNetworkConnections","GetNetworkConnections method [Network Awareness]","GetNetworkConnections method [Network Awareness]","INetwork interface","INetwork interface [Network Awareness]","GetNetworkConnections method","INetwork.GetNetworkConnections","INetwork::GetNetworkConnections","netlistmgr/INetwork::GetNetworkConnections","nla.inetwork_getnetworkconnections"]
old-location: nla\inetwork_getnetworkconnections.htm
tech.root: nla
ms.assetid: cc599537-3c31-4674-81d0-608cadae3e61
ms.date: 12/05/2018
ms.keywords: GetNetworkConnections, GetNetworkConnections method [Network Awareness], GetNetworkConnections method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetNetworkConnections method, INetwork.GetNetworkConnections, INetwork::GetNetworkConnections, netlistmgr/INetwork::GetNetworkConnections, nla.inetwork_getnetworkconnections
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
 - INetwork::GetNetworkConnections
 - netlistmgr/INetwork::GetNetworkConnections
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
 - INetwork.GetNetworkConnections
---

# INetwork::GetNetworkConnections


## -description

The <b>GetNetworkConnections</b> method returns an enumeration of all network connections for a network. A network can have multiple connections to it from different interfaces or different links from the same interface.

## -parameters

### -param ppEnumNetworkConnection [out]

Pointer to an <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-ienumnetworkconnections">IEnumNetworkConnections</a> interface instance that enumerates the list of local connections to this network.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a>