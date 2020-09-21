---
UID: NF:netlistmgr.INetwork.get_IsConnected
title: INetwork::get_IsConnected (netlistmgr.h)
description: The get_IsConnected property specifies if the network has any network connectivity.
helpviewer_keywords: ["INetwork interface [Network Awareness]","get_IsConnected method","INetwork.get_IsConnected","INetwork::get_IsConnected","get_IsConnected","get_IsConnected method [Network Awareness]","get_IsConnected method [Network Awareness]","INetwork interface","netlistmgr/INetwork::get_IsConnected","nla.inetwork_get_isconnected"]
old-location: nla\inetwork_get_isconnected.htm
tech.root: nla
ms.assetid: 24bfcd98-b9c3-44f5-9f7b-13c05dcc8974
ms.date: 12/05/2018
ms.keywords: INetwork interface [Network Awareness],get_IsConnected method, INetwork.get_IsConnected, INetwork::get_IsConnected, get_IsConnected, get_IsConnected method [Network Awareness], get_IsConnected method [Network Awareness],INetwork interface, netlistmgr/INetwork::get_IsConnected, nla.inetwork_get_isconnected
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
 - INetwork::get_IsConnected
 - netlistmgr/INetwork::get_IsConnected
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
 - INetwork.get_IsConnected
---

# INetwork::get_IsConnected


## -description

The <b>get_IsConnected</b> property specifies if the network has any network connectivity.

## -parameters

### -param pbIsConnected [out]

If <b>TRUE</b>, this network is connected; if <b>FALSE</b>, it is not.

## -returns

Returns S_OK if successful.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a>