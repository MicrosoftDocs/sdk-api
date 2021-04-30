---
UID: NF:netlistmgr.INetworkConnection.GetConnectionId
title: INetworkConnection::GetConnectionId (netlistmgr.h)
description: The GetConnectionID method returns the Connection ID associated with this network connection.
helpviewer_keywords: ["GetConnectionId","GetConnectionId method [Network Awareness]","GetConnectionId method [Network Awareness]","INetworkConnection interface","INetworkConnection interface [Network Awareness]","GetConnectionId method","INetworkConnection.GetConnectionId","INetworkConnection::GetConnectionId","netlistmgr/INetworkConnection::GetConnectionId","nla.inetworkconnection_getconnectionid"]
old-location: nla\inetworkconnection_getconnectionid.htm
tech.root: nla
ms.assetid: c8619fd1-2764-4f20-a258-fb4368e448b7
ms.date: 12/05/2018
ms.keywords: GetConnectionId, GetConnectionId method [Network Awareness], GetConnectionId method [Network Awareness],INetworkConnection interface, INetworkConnection interface [Network Awareness],GetConnectionId method, INetworkConnection.GetConnectionId, INetworkConnection::GetConnectionId, netlistmgr/INetworkConnection::GetConnectionId, nla.inetworkconnection_getconnectionid
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
 - INetworkConnection::GetConnectionId
 - netlistmgr/INetworkConnection::GetConnectionId
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
 - INetworkConnection.GetConnectionId
---

# INetworkConnection::GetConnectionId


## -description

The <a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnection-getadapterid">GetConnectionID</a> method returns the Connection ID associated with this network connection.

## -parameters

### -param pgdConnectionId [out]

Pointer to a <b>GUID</b> that specifies the Connection ID associated with this network connection.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnection">INetworkConnection</a>