---
UID: NF:netlistmgr.INetworkEvents.NetworkDeleted
title: INetworkEvents::NetworkDeleted (netlistmgr.h)
description: The NetworkDeleted method is called when a network is deleted.
helpviewer_keywords: ["INetworkEvents interface [Network Awareness]","NetworkDeleted method","INetworkEvents.NetworkDeleted","INetworkEvents::NetworkDeleted","NetworkDeleted","NetworkDeleted method [Network Awareness]","NetworkDeleted method [Network Awareness]","INetworkEvents interface","netlistmgr/INetworkEvents::NetworkDeleted","nla.inetworkevents_networkdeleted"]
old-location: nla\inetworkevents_networkdeleted.htm
tech.root: nla
ms.assetid: ae54cc29-6da8-405d-92f9-654239150dd0
ms.date: 12/05/2018
ms.keywords: INetworkEvents interface [Network Awareness],NetworkDeleted method, INetworkEvents.NetworkDeleted, INetworkEvents::NetworkDeleted, NetworkDeleted, NetworkDeleted method [Network Awareness], NetworkDeleted method [Network Awareness],INetworkEvents interface, netlistmgr/INetworkEvents::NetworkDeleted, nla.inetworkevents_networkdeleted
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
 - INetworkEvents::NetworkDeleted
 - netlistmgr/INetworkEvents::NetworkDeleted
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
 - INetworkEvents.NetworkDeleted
---

# INetworkEvents::NetworkDeleted


## -description

The <b>NetworkDeleted</b> method is called when a network is deleted.

## -parameters

### -param networkId [in]

GUID that contains the network ID of the network that was deleted.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkevents">INetworkEvents</a>