---
UID: NF:netlistmgr.INetworkCostManagerEvents.CostChanged
title: INetworkCostManagerEvents::CostChanged (netlistmgr.h)
description: CostChanged method is called to indicates a cost change for either machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.
helpviewer_keywords: ["CostChanged","CostChanged method [Network Awareness]","CostChanged method [Network Awareness]","INetworkCostManagerEvents interface","INetworkCostManagerEvents interface [Network Awareness]","CostChanged method","INetworkCostManagerEvents.CostChanged","INetworkCostManagerEvents::CostChanged","netlistmgr/INetworkCostManagerEvents::CostChanged","nla.inetworkcostmanagerevents_costchanged"]
old-location: nla\inetworkcostmanagerevents_costchanged.htm
tech.root: nla
ms.assetid: 39262F6A-9701-4917-BBDF-1BAC201585D4
ms.date: 12/05/2018
ms.keywords: CostChanged, CostChanged method [Network Awareness], CostChanged method [Network Awareness],INetworkCostManagerEvents interface, INetworkCostManagerEvents interface [Network Awareness],CostChanged method, INetworkCostManagerEvents.CostChanged, INetworkCostManagerEvents::CostChanged, netlistmgr/INetworkCostManagerEvents::CostChanged, nla.inetworkcostmanagerevents_costchanged
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
 - INetworkCostManagerEvents::CostChanged
 - netlistmgr/INetworkCostManagerEvents::CostChanged
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
 - INetworkCostManagerEvents.CostChanged
---

# INetworkCostManagerEvents::CostChanged


## -description

The <b>CostChanged</b> method is called to indicates a cost change for either machine-wide Internet connectivity, or the first-hop of routing to a specific destination on a connection.

## -parameters

### -param newCost [in]

A DWORD that represents the new cost of the connection. The lowest 16 bits represent the cost level, and the highest 16 bits represent the flags. Possible values are defined by the <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connection_cost">NLM_CONNECTION_COST</a> enumeration.

### -param pDestAddr [in]

An <a href="/windows/desktop/api/netlistmgr/ns-netlistmgr-nlm_sockaddr">NLM_SOCKADDR</a> structure containing an IPv4/IPv6 address that identifies the destination on which the event occurred. If <i>destAddr</i> is NULL, the change is a machine-wide Internet connectivity change.

## -returns

Returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nn-netlistmgr-inetworkcostmanagerevents">INetworkCostManagerEvents</a>