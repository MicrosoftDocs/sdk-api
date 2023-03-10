---
UID: NF:netlistmgr.INetworkEvents.NetworkPropertyChanged
title: INetworkEvents::NetworkPropertyChanged (netlistmgr.h)
description: The NetworkPropertyChanged method is called when a network property change is detected.
helpviewer_keywords: ["INetworkEvents interface [Network Awareness]","NetworkPropertyChanged method","INetworkEvents.NetworkPropertyChanged","INetworkEvents::NetworkPropertyChanged","NetworkPropertyChanged","NetworkPropertyChanged method [Network Awareness]","NetworkPropertyChanged method [Network Awareness]","INetworkEvents interface","netlistmgr/INetworkEvents::NetworkPropertyChanged","nla.inetworkevents_networkpropertychanged"]
old-location: nla\inetworkevents_networkpropertychanged.htm
tech.root: nla
ms.assetid: a84f49ee-9efd-450e-a6e6-3f140330a9d0
ms.date: 12/05/2018
ms.keywords: INetworkEvents interface [Network Awareness],NetworkPropertyChanged method, INetworkEvents.NetworkPropertyChanged, INetworkEvents::NetworkPropertyChanged, NetworkPropertyChanged, NetworkPropertyChanged method [Network Awareness], NetworkPropertyChanged method [Network Awareness],INetworkEvents interface, netlistmgr/INetworkEvents::NetworkPropertyChanged, nla.inetworkevents_networkpropertychanged
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
 - INetworkEvents::NetworkPropertyChanged
 - netlistmgr/INetworkEvents::NetworkPropertyChanged
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
 - INetworkEvents.NetworkPropertyChanged
---

# INetworkEvents::NetworkPropertyChanged


## -description

The <b>NetworkPropertyChanged</b> method is called when a network property change is detected.

## -parameters

### -param networkId [in]

GUID that specifies the network on which this event occurred.

### -param flags [in]

<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_network_property_change">NLM_NETWORK_PROPERTY_CHANGE</a> enumeration value that specifies the network property that changed.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkevents">INetworkEvents</a>



<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_network_property_change">NLM_NETWORK_PROPERTY_CHANGE</a>