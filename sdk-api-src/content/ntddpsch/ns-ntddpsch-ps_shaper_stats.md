---
UID: NS:ntddpsch._PS_SHAPER_STATS
title: PS_SHAPER_STATS (ntddpsch.h)
description: The PS_SHAPER_STATS structure provides statistical packet shaper information about the computer's packet shaper component. Note that the PS_SHAPER_STATS structure is used in conjunction with the PS_COMPONENT_STATS structure.
helpviewer_keywords: ["*PPS_SHAPER_STATS","PPS_SHAPER_STATS","PPS_SHAPER_STATS structure pointer [QOS]","PS_SHAPER_STATS","PS_SHAPER_STATS structure [QOS]","_gqos_ps_shaper_stats","ntddpsch/PPS_SHAPER_STATS","ntddpsch/PS_SHAPER_STATS","qos.ps_shaper_stats"]
old-location: qos\ps_shaper_stats.htm
tech.root: QOS
ms.assetid: fd2ef45d-154a-47b0-ba40-a823f9dd6dce
ms.date: 12/05/2018
ms.keywords: '*PPS_SHAPER_STATS, PPS_SHAPER_STATS, PPS_SHAPER_STATS structure pointer [QOS], PS_SHAPER_STATS, PS_SHAPER_STATS structure [QOS], _gqos_ps_shaper_stats, ntddpsch/PPS_SHAPER_STATS, ntddpsch/PS_SHAPER_STATS, qos.ps_shaper_stats'
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
req.typenames: PS_SHAPER_STATS, *PPS_SHAPER_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PS_SHAPER_STATS
 - ntddpsch/_PS_SHAPER_STATS
 - PPS_SHAPER_STATS
 - ntddpsch/PPS_SHAPER_STATS
 - PS_SHAPER_STATS
 - ntddpsch/PS_SHAPER_STATS
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
 - PS_SHAPER_STATS
---

# PS_SHAPER_STATS structure


## -description

The 
<b>PS_SHAPER_STATS</b> structure provides statistical packet shaper information about the computer's packet shaper component. Note that the 
<b>PS_SHAPER_STATS</b> structure is used in conjunction with the 
<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_component_stats">PS_COMPONENT_STATS</a> structure.

## -struct-fields

### -field MaxPacketsInShaper

Maximum number of packets that have been in the packet shaper for the flow or interface.

### -field AveragePacketsInShaper

Average number of packets that have been in the packet shaper for the flow or interface.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_component_stats">PS_COMPONENT_STATS</a>