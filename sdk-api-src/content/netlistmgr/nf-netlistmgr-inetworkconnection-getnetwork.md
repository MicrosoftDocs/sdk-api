---
UID: NF:netlistmgr.INetworkConnection.GetNetwork
title: INetworkConnection::GetNetwork (netlistmgr.h)
description: The GetNetwork method returns the network associated with the connection.
helpviewer_keywords: ["GetNetwork","GetNetwork method [Network Awareness]","GetNetwork method [Network Awareness]","INetworkConnection interface","INetworkConnection interface [Network Awareness]","GetNetwork method","INetworkConnection.GetNetwork","INetworkConnection::GetNetwork","netlistmgr/INetworkConnection::GetNetwork","nla.inetworkconnection_getnetwork"]
old-location: nla\inetworkconnection_getnetwork.htm
tech.root: nla
ms.assetid: 7de83422-58f6-40fc-b26f-074cec550247
ms.date: 12/05/2018
ms.keywords: GetNetwork, GetNetwork method [Network Awareness], GetNetwork method [Network Awareness],INetworkConnection interface, INetworkConnection interface [Network Awareness],GetNetwork method, INetworkConnection.GetNetwork, INetworkConnection::GetNetwork, netlistmgr/INetworkConnection::GetNetwork, nla.inetworkconnection_getnetwork
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
 - INetworkConnection::GetNetwork
 - netlistmgr/INetworkConnection::GetNetwork
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
 - INetworkConnection.GetNetwork
---

# INetworkConnection::GetNetwork


## -description

The <b>GetNetwork</b> method returns the network associated with the connection.

## -parameters

### -param ppNetwork [out]

Pointer to a pointer that receives an <a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a> interface instance that specifies the network associated with the connection.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a>