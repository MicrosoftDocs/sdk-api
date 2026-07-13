---
UID: NF:netlistmgr.INetworkEvents.NetworkConnectivityChanged
title: INetworkEvents::NetworkConnectivityChanged (netlistmgr.h)
description: The NetworkConnectivityChanged method is called when network connectivity related changes occur. (INetworkEvents.NetworkConnectivityChanged)
helpviewer_keywords: ["INetworkEvents interface [Network Awareness]","NetworkConnectivityChanged method","INetworkEvents.NetworkConnectivityChanged","INetworkEvents::NetworkConnectivityChanged","NetworkConnectivityChanged","NetworkConnectivityChanged method [Network Awareness]","NetworkConnectivityChanged method [Network Awareness]","INetworkEvents interface","netlistmgr/INetworkEvents::NetworkConnectivityChanged","nla.inetworkevents_networkconnectivitychanged"]
old-location: nla\inetworkevents_networkconnectivitychanged.htm
tech.root: nla
ms.assetid: adaf3abe-9a8c-45af-bcc7-bcc516ed75ff
ms.date: 12/05/2018
ms.keywords: INetworkEvents interface [Network Awareness],NetworkConnectivityChanged method, INetworkEvents.NetworkConnectivityChanged, INetworkEvents::NetworkConnectivityChanged, NetworkConnectivityChanged, NetworkConnectivityChanged method [Network Awareness], NetworkConnectivityChanged method [Network Awareness],INetworkEvents interface, netlistmgr/INetworkEvents::NetworkConnectivityChanged, nla.inetworkevents_networkconnectivitychanged
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
 - INetworkEvents::NetworkConnectivityChanged
 - netlistmgr/INetworkEvents::NetworkConnectivityChanged
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
 - INetworkEvents.NetworkConnectivityChanged
---

# INetworkEvents::NetworkConnectivityChanged


## -description

The <b>NetworkConnectivityChanged</b> method is called when network connectivity related changes occur.

## -parameters

### -param networkId [in]

 A <b>GUID</b> that specifies the new network that was added.

### -param newConnectivity [in]

<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a> enumeration value that contains the new connectivity of this network.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkevents">INetworkEvents</a>



<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connectivity">NLM_CONNECTIVITY</a>
