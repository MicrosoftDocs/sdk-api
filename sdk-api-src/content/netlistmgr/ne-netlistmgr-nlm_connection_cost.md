---
UID: NE:netlistmgr.NLM_CONNECTION_COST
title: NLM_CONNECTION_COST (netlistmgr.h)
description: The NLM_CONNECTION_COST enumeration specifies a set of cost levels and cost flags supported in Windows 8 Cost APIs.
helpviewer_keywords: ["NLM_CONNECTION_COST","NLM_CONNECTION_COST enumeration [Network Awareness]","NLM_CONNECTION_COST_APPROACHINGDATALIMIT","NLM_CONNECTION_COST_CONGESTED","NLM_CONNECTION_COST_FIXED","NLM_CONNECTION_COST_OVERDATALIMIT","NLM_CONNECTION_COST_ROAMING","NLM_CONNECTION_COST_UNKNOWN","NLM_CONNECTION_COST_UNRESTRICTED","NLM_CONNECTION_COST_VARIABLE","netlistmgr/NLM_CONNECTION_COST","netlistmgr/NLM_CONNECTION_COST_APPROACHINGDATALIMIT","netlistmgr/NLM_CONNECTION_COST_CONGESTED","netlistmgr/NLM_CONNECTION_COST_FIXED","netlistmgr/NLM_CONNECTION_COST_OVERDATALIMIT","netlistmgr/NLM_CONNECTION_COST_ROAMING","netlistmgr/NLM_CONNECTION_COST_UNKNOWN","netlistmgr/NLM_CONNECTION_COST_UNRESTRICTED","netlistmgr/NLM_CONNECTION_COST_VARIABLE","nla.nlm_connection_cost"]
old-location: nla\nlm_connection_cost.htm
tech.root: nla
ms.assetid: 93541814-A1C3-4C24-BB99-CEE4895F34F8
ms.date: 12/05/2018
ms.keywords: NLM_CONNECTION_COST, NLM_CONNECTION_COST enumeration [Network Awareness], NLM_CONNECTION_COST_APPROACHINGDATALIMIT, NLM_CONNECTION_COST_CONGESTED, NLM_CONNECTION_COST_FIXED, NLM_CONNECTION_COST_OVERDATALIMIT, NLM_CONNECTION_COST_ROAMING, NLM_CONNECTION_COST_UNKNOWN, NLM_CONNECTION_COST_UNRESTRICTED, NLM_CONNECTION_COST_VARIABLE, netlistmgr/NLM_CONNECTION_COST, netlistmgr/NLM_CONNECTION_COST_APPROACHINGDATALIMIT, netlistmgr/NLM_CONNECTION_COST_CONGESTED, netlistmgr/NLM_CONNECTION_COST_FIXED, netlistmgr/NLM_CONNECTION_COST_OVERDATALIMIT, netlistmgr/NLM_CONNECTION_COST_ROAMING, netlistmgr/NLM_CONNECTION_COST_UNKNOWN, netlistmgr/NLM_CONNECTION_COST_UNRESTRICTED, netlistmgr/NLM_CONNECTION_COST_VARIABLE, nla.nlm_connection_cost
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
req.typenames: NLM_CONNECTION_COST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NLM_CONNECTION_COST
 - netlistmgr/NLM_CONNECTION_COST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netlistmgr.h
api_name:
 - NLM_CONNECTION_COST
---

# NLM_CONNECTION_COST enumeration


## -description

The <b>NLM_CONNECTION_COST</b> enumeration specifies a set of cost levels and cost flags supported in Windows 8 Cost APIs.

## -enum-fields

### -field NLM_CONNECTION_COST_UNKNOWN:0

The cost is unknown.

### -field NLM_CONNECTION_COST_UNRESTRICTED:0x1

The connection is unlimited and is considered to be unrestricted of usage charges and capacity constraints.

### -field NLM_CONNECTION_COST_FIXED:0x2

The use of this connection is unrestricted up to a specific data transfer limit.

### -field NLM_CONNECTION_COST_VARIABLE:0x4

This connection is regulated on a per byte basis.

### -field NLM_CONNECTION_COST_OVERDATALIMIT:0x10000

The connection is currently in an OverDataLimit state as it has exceeded the carrier specified data transfer limit.

### -field NLM_CONNECTION_COST_CONGESTED:0x20000

The network is experiencing high traffic load and is congested.

### -field NLM_CONNECTION_COST_ROAMING:0x40000

The connection is roaming outside the network and  affiliates of the home provider.

### -field NLM_CONNECTION_COST_APPROACHINGDATALIMIT:0x80000

The connection is approaching the data limit specified by the carrier.

## -remarks

The value returned by the <a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnectioncost-getcost">INetworkConnectionCost::GetCost</a> method can have multiple bits set with the values specified by this enumeration.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkconnectioncost-getcost">INetworkConnectionCost::GetCost</a>
