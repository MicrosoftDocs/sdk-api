---
UID: NF:netlistmgr.INetworkConnectionCostEvents.ConnectionCostChanged
title: INetworkConnectionCostEvents::ConnectionCostChanged (netlistmgr.h)
description: ConnectionCostChanged method notifies an application of a network cost change for a connection.
helpviewer_keywords: ["ConnectionCostChanged","ConnectionCostChanged method [Network Awareness]","ConnectionCostChanged method [Network Awareness]","INetworkConnectionCostEvents interface","INetworkConnectionCostEvents interface [Network Awareness]","ConnectionCostChanged method","INetworkConnectionCostEvents.ConnectionCostChanged","INetworkConnectionCostEvents::ConnectionCostChanged","netlistmgr/INetworkConnectionCostEvents::ConnectionCostChanged","nla.inetworkconnectioncostevents_connectioncostchanged"]
old-location: nla\inetworkconnectioncostevents_connectioncostchanged.htm
tech.root: nla
ms.assetid: 85D0BF59-3E06-4978-8400-71FD7BF990C9
ms.date: 12/05/2018
ms.keywords: ConnectionCostChanged, ConnectionCostChanged method [Network Awareness], ConnectionCostChanged method [Network Awareness],INetworkConnectionCostEvents interface, INetworkConnectionCostEvents interface [Network Awareness],ConnectionCostChanged method, INetworkConnectionCostEvents.ConnectionCostChanged, INetworkConnectionCostEvents::ConnectionCostChanged, netlistmgr/INetworkConnectionCostEvents::ConnectionCostChanged, nla.inetworkconnectioncostevents_connectioncostchanged
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - INetworkConnectionCostEvents::ConnectionCostChanged
 - netlistmgr/INetworkConnectionCostEvents::ConnectionCostChanged
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
 - INetworkConnectionCostEvents.ConnectionCostChanged
---

# INetworkConnectionCostEvents::ConnectionCostChanged


## -description

The <b>ConnectionCostChanged</b> method notifies an application of a network cost change for a connection.

## -parameters

### -param connectionId [in]

A unique ID  that identifies the connection on which the cost change event occurred.

### -param newCost [in]

A DWORD value that represents the new cost of the connection. The lowest 16 bits represent the cost level, and the highest 16 bits represent the flags. Possible values are defined by the <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connection_cost">NLM_CONNECTION_COST</a> enumeration.

## -returns

This method returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkconnectioncostevents">INetworkConnectionCostEvents</a>