---
UID: NS:ntddpsch._PS_ADAPTER_STATS
title: PS_ADAPTER_STATS (ntddpsch.h)
description: The PS_ADAPTER_STATS structure provides statistical packet shaper information about a specified adapter. Note that the PS_ADAPTER_STATS structure is used in conjunction with the PS_COMPONENT_STATS structure.
helpviewer_keywords: ["*PPS_ADAPTER_STATS","PPS_ADAPTER_STATS","PPS_ADAPTER_STATS structure pointer [QOS]","PS_ADAPTER_STATS","PS_ADAPTER_STATS structure [QOS]","_gqos_ps_adapter_stats","ntddpsch/PPS_ADAPTER_STATS","ntddpsch/PS_ADAPTER_STATS","qos.ps_adapter_stats"]
old-location: qos\ps_adapter_stats.htm
tech.root: QOS
ms.assetid: 365b3987-9a7a-4c15-980d-aa39956c68c8
ms.date: 12/05/2018
ms.keywords: '*PPS_ADAPTER_STATS, PPS_ADAPTER_STATS, PPS_ADAPTER_STATS structure pointer [QOS], PS_ADAPTER_STATS, PS_ADAPTER_STATS structure [QOS], _gqos_ps_adapter_stats, ntddpsch/PPS_ADAPTER_STATS, ntddpsch/PS_ADAPTER_STATS, qos.ps_adapter_stats'
req.header: ntddpsch.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PS_ADAPTER_STATS, *PPS_ADAPTER_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PS_ADAPTER_STATS
 - ntddpsch/_PS_ADAPTER_STATS
 - PPS_ADAPTER_STATS
 - ntddpsch/PPS_ADAPTER_STATS
 - PS_ADAPTER_STATS
 - ntddpsch/PS_ADAPTER_STATS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntddpsch.h
api_name:
 - PS_ADAPTER_STATS
---

# PS_ADAPTER_STATS structure


## -description

The 
<b>PS_ADAPTER_STATS</b> structure provides statistical packet shaper information about a specified adapter. Note that the 
<b>PS_ADAPTER_STATS</b> structure is used in conjunction with the 
<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_component_stats">PS_COMPONENT_STATS</a> structure.

## -struct-fields

### -field OutOfPackets

Number of instances in which the adapter had no packets to transmit on the specified adapter.

### -field FlowsOpened

Number of flows opened on the adapter.

### -field FlowsClosed

Number of flows closed on the adapter.

### -field FlowsRejected

Number of flows that were rejected due to packet shaper constraints on the adapter.

### -field FlowsModified

Number of flows that were modified on the adapter.

### -field FlowModsRejected

Number of flow modifications that were rejected on the adapter due to packet shaper constraints.

### -field MaxSimultaneousFlows

Maximum number of simultaneous flows.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_component_stats">PS_COMPONENT_STATS</a>