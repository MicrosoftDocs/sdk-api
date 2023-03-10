---
UID: NS:ntddpsch._PS_CONFORMER_STATS
title: PS_CONFORMER_STATS (ntddpsch.h)
description: The PS_CONFORMER_STATS structure provides statistical packet shaper information about a particular flow. Note that the PS_CONFORMER_STATS structure is used in conjunction with the PS_COMPONENT_STATS structure.
helpviewer_keywords: ["*PPS_CONFORMER_STATS","PPS_CONFORMER_STATS","PPS_CONFORMER_STATS structure pointer [QOS]","PS_CONFORMER_STATS","PS_CONFORMER_STATS structure [QOS]","_gqos_ps_conformer_stats","ntddpsch/PPS_CONFORMER_STATS","ntddpsch/PS_CONFORMER_STATS","qos.ps_conformer_stats"]
old-location: qos\ps_conformer_stats.htm
tech.root: QOS
ms.assetid: 709274fe-de56-4f86-9002-71f0ee333ace
ms.date: 12/05/2018
ms.keywords: '*PPS_CONFORMER_STATS, PPS_CONFORMER_STATS, PPS_CONFORMER_STATS structure pointer [QOS], PS_CONFORMER_STATS, PS_CONFORMER_STATS structure [QOS], _gqos_ps_conformer_stats, ntddpsch/PPS_CONFORMER_STATS, ntddpsch/PS_CONFORMER_STATS, qos.ps_conformer_stats'
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
req.typenames: PS_CONFORMER_STATS, *PPS_CONFORMER_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PS_CONFORMER_STATS
 - ntddpsch/_PS_CONFORMER_STATS
 - PPS_CONFORMER_STATS
 - ntddpsch/PPS_CONFORMER_STATS
 - PS_CONFORMER_STATS
 - ntddpsch/PS_CONFORMER_STATS
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
 - PS_CONFORMER_STATS
---

# PS_CONFORMER_STATS structure


## -description

The 
<b>PS_CONFORMER_STATS</b> structure provides statistical packet shaper information about a particular flow. Note that the 
<b>PS_CONFORMER_STATS</b> structure is used in conjunction with the 
<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_component_stats">PS_COMPONENT_STATS</a> structure.

## -struct-fields

### -field NonconformingPacketsScheduled

Number of nonconforming packets that have been scheduled on the flow or interface.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_component_stats">PS_COMPONENT_STATS</a>