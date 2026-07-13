---
UID: NS:ntddpsch._PS_DRRSEQ_STATS
title: PS_DRRSEQ_STATS (ntddpsch.h)
description: The PS_DRRSEQ_STATS structure provides network interface card (NIC) and packet sequencer and packet shaper statistics. Note that the PS_DRRSEQ_STATS structure is used in conjunction with the PS_COMPONENT_STATS structure.
helpviewer_keywords: ["*PPS_DRRSEQ_STATS","PPS_DRRSEQ_STATS","PPS_DRRSEQ_STATS structure pointer [QOS]","PS_DRRSEQ_STATS","PS_DRRSEQ_STATS structure [QOS]","_gqos_ps_drrseq_stats","ntddpsch/PPS_DRRSEQ_STATS","ntddpsch/PS_DRRSEQ_STATS","qos.ps_drrseq_stats"]
old-location: qos\ps_drrseq_stats.htm
tech.root: QOS
ms.assetid: c8d5bf61-5a19-4bbd-ae4c-0502b6803191
ms.date: 12/05/2018
ms.keywords: '*PPS_DRRSEQ_STATS, PPS_DRRSEQ_STATS, PPS_DRRSEQ_STATS structure pointer [QOS], PS_DRRSEQ_STATS, PS_DRRSEQ_STATS structure [QOS], _gqos_ps_drrseq_stats, ntddpsch/PPS_DRRSEQ_STATS, ntddpsch/PS_DRRSEQ_STATS, qos.ps_drrseq_stats'
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
req.typenames: PS_DRRSEQ_STATS, *PPS_DRRSEQ_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PS_DRRSEQ_STATS
 - ntddpsch/_PS_DRRSEQ_STATS
 - PPS_DRRSEQ_STATS
 - ntddpsch/PPS_DRRSEQ_STATS
 - PS_DRRSEQ_STATS
 - ntddpsch/PS_DRRSEQ_STATS
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
 - PS_DRRSEQ_STATS
---

# PS_DRRSEQ_STATS structure


## -description

The 
<b>PS_DRRSEQ_STATS</b> structure provides network interface card (NIC) and packet sequencer–packet shaper statistics. Note that the 
<b>PS_DRRSEQ_STATS</b> structure is used in conjunction with the 
<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_component_stats">PS_COMPONENT_STATS</a> structure.

## -struct-fields

### -field MaxPacketsInNetcard

Maximum number of packets that have been queued in the network interface card for the flow or interface.

### -field AveragePacketsInNetcard

Average number of packets queued in the network interface card for the flow or interface.

### -field MaxPacketsInSequencer

Maximum number of packets that have been queued in the packet sequencer for the flow or interface.

### -field AveragePacketsInSequencer

Average number of packets that have been queued in the packet sequencer for the flow or interface.

### -field NonconformingPacketsTransmitted

Number of nonconforming packets that have been transmitted for the flow or interface.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_component_stats">PS_COMPONENT_STATS</a>
