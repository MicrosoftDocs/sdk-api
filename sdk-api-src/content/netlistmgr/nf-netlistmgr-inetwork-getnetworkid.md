---
UID: NF:netlistmgr.INetwork.GetNetworkId
title: INetwork::GetNetworkId (netlistmgr.h)
description: The GetNetworkId method returns the unique identifier of a network.
helpviewer_keywords: ["GetNetworkId","GetNetworkId method [Network Awareness]","GetNetworkId method [Network Awareness]","INetwork interface","INetwork interface [Network Awareness]","GetNetworkId method","INetwork.GetNetworkId","INetwork::GetNetworkId","netlistmgr/INetwork::GetNetworkId","nla.inetwork_getnetworkid"]
old-location: nla\inetwork_getnetworkid.htm
tech.root: nla
ms.assetid: f2012295-d443-434f-8fe8-b6e38e7cac74
ms.date: 12/05/2018
ms.keywords: GetNetworkId, GetNetworkId method [Network Awareness], GetNetworkId method [Network Awareness],INetwork interface, INetwork interface [Network Awareness],GetNetworkId method, INetwork.GetNetworkId, INetwork::GetNetworkId, netlistmgr/INetwork::GetNetworkId, nla.inetwork_getnetworkid
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
 - INetwork::GetNetworkId
 - netlistmgr/INetwork::GetNetworkId
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
 - INetwork.GetNetworkId
---

# INetwork::GetNetworkId


## -description

The <b>GetNetworkId</b> method returns the unique identifier of a network.

## -parameters

### -param pgdGuidNetworkId [out]

Pointer to a GUID that specifies the network ID.

## -returns

Returns S_OK if the method succeeds.

## -remarks

The caller is responsible for allocating the buffer pointed to by <i>pgdGuidNetworkId</i>. This buffer must be large enough to hold a GUID. 

Calling  <b>GetNetworkId</b> will return S_OK even if the network requested has been deleted.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetwork">INetwork</a>