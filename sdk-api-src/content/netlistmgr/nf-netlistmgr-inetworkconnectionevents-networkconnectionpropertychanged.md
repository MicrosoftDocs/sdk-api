---
UID: NF:netlistmgr.INetworkConnectionEvents.NetworkConnectionPropertyChanged
title: INetworkConnectionEvents::NetworkConnectionPropertyChanged (netlistmgr.h)
description: The NetworkConnectionPropertyChanged method notifies a client when property change events related to a specific network connection occur.
helpviewer_keywords: ["INetworkConnectionEvents interface [Network Awareness]","NetworkConnectionPropertyChanged method","INetworkConnectionEvents.NetworkConnectionPropertyChanged","INetworkConnectionEvents::NetworkConnectionPropertyChanged","NetworkConnectionPropertyChanged","NetworkConnectionPropertyChanged method [Network Awareness]","NetworkConnectionPropertyChanged method [Network Awareness]","INetworkConnectionEvents interface","netlistmgr/INetworkConnectionEvents::NetworkConnectionPropertyChanged","nla.inetworkconnectionevents_networkconnectionpropertychange"]
old-location: nla\inetworkconnectionevents_networkconnectionpropertychange.htm
tech.root: nla
ms.assetid: 38c6a422-9291-4136-ac81-b634040138b3
ms.date: 12/05/2018
ms.keywords: INetworkConnectionEvents interface [Network Awareness],NetworkConnectionPropertyChanged method, INetworkConnectionEvents.NetworkConnectionPropertyChanged, INetworkConnectionEvents::NetworkConnectionPropertyChanged, NetworkConnectionPropertyChanged, NetworkConnectionPropertyChanged method [Network Awareness], NetworkConnectionPropertyChanged method [Network Awareness],INetworkConnectionEvents interface, netlistmgr/INetworkConnectionEvents::NetworkConnectionPropertyChanged, nla.inetworkconnectionevents_networkconnectionpropertychange
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
 - INetworkConnectionEvents::NetworkConnectionPropertyChanged
 - netlistmgr/INetworkConnectionEvents::NetworkConnectionPropertyChanged
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
 - INetworkConnectionEvents.NetworkConnectionPropertyChanged
---

# INetworkConnectionEvents::NetworkConnectionPropertyChanged


## -description

The <b>NetworkConnectionPropertyChanged</b> method notifies a client when property change events related to a specific network connection occur.

## -parameters

### -param connectionId [in]

A GUID that identifies the network connection  on which the event occurred.

### -param flags [in]

The <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connection_property_change">NLM_CONNECTION_PROPERTY_CHANGE</a> flags for this connection.

## -returns

Returns S_OK if the method succeeds.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnectionevents">INetworkConnectionEvents</a>



<a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connection_property_change">NLM_CONNECTION_PROPERTY_CHANGE</a>