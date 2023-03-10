---
UID: NS:ntddpsch._PS_FLOW_STATS
title: PS_FLOW_STATS (ntddpsch.h)
description: The PS_FLOW_STATS structure provides statistical packet shaper information about a particular flow. Note that the PS_FLOW_STATS structure is used in conjunction with the PS_COMPONENT_STATS structure.
helpviewer_keywords: ["*PPS_FLOW_STATS","PPS_FLOW_STATS","PPS_FLOW_STATS structure pointer [QOS]","PS_FLOW_STATS","PS_FLOW_STATS structure [QOS]","_gqos_ps_flow_stats","ntddpsch/PPS_FLOW_STATS","ntddpsch/PS_FLOW_STATS","qos.ps_flow_stats"]
old-location: qos\ps_flow_stats.htm
tech.root: QOS
ms.assetid: 1d40c247-9e61-4f8b-85f9-eddc90727a17
ms.date: 12/05/2018
ms.keywords: '*PPS_FLOW_STATS, PPS_FLOW_STATS, PPS_FLOW_STATS structure pointer [QOS], PS_FLOW_STATS, PS_FLOW_STATS structure [QOS], _gqos_ps_flow_stats, ntddpsch/PPS_FLOW_STATS, ntddpsch/PS_FLOW_STATS, qos.ps_flow_stats'
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
req.typenames: PS_FLOW_STATS, *PPS_FLOW_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PS_FLOW_STATS
 - ntddpsch/_PS_FLOW_STATS
 - PPS_FLOW_STATS
 - ntddpsch/PPS_FLOW_STATS
 - PS_FLOW_STATS
 - ntddpsch/PS_FLOW_STATS
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
 - PS_FLOW_STATS
---

# PS_FLOW_STATS structure


## -description

The 
<b>PS_FLOW_STATS</b> structure provides statistical packet shaper information about a particular flow. Note that the 
<b>PS_FLOW_STATS</b> structure is used in conjunction with the 
<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_component_stats">PS_COMPONENT_STATS</a> structure.

## -struct-fields

### -field DroppedPackets

Number of packets that have been dropped from the flow.

### -field PacketsScheduled

Number of packets that have been scheduled for transmission on the flow.

### -field PacketsTransmitted

Number of packets that have been transmitted on the flow.

### -field BytesScheduled

Number of bytes that have been scheduled for transmission on the flow.

### -field BytesTransmitted

Number of bytes that have been transmitted on the flow.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_component_stats">PS_COMPONENT_STATS</a>