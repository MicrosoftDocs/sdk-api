---
UID: NS:ntddpsch._PS_COMPONENT_STATS
title: PS_COMPONENT_STATS (ntddpsch.h)
description: The PS_COMPONENT_STATS structure enables applications to get statistical information regarding their TC-enabled flow.
helpviewer_keywords: ["*PPS_COMPONENT_STATS","PPS_COMPONENT_STATS","PPS_COMPONENT_STATS structure pointer [QOS]","PS_ADAPTER_STATS (1)","PS_COMPONENT_STATS","PS_COMPONENT_STATS structure [QOS]","PS_CONFORMER_STATS (3)","PS_DRRSEQ_STATS (5)","PS_FLOW_STATS (2)","PS_SHAPER_STATS (4)","_gqos_ps_component_stats","ntddpsch/PPS_COMPONENT_STATS","ntddpsch/PS_COMPONENT_STATS","qos.ps_component_stats"]
old-location: qos\ps_component_stats.htm
tech.root: QOS
ms.assetid: 6263d80a-5486-4748-b3a7-4c9d9bb2162f
ms.date: 12/05/2018
ms.keywords: '*PPS_COMPONENT_STATS, PPS_COMPONENT_STATS, PPS_COMPONENT_STATS structure pointer [QOS], PS_ADAPTER_STATS (1), PS_COMPONENT_STATS, PS_COMPONENT_STATS structure [QOS], PS_CONFORMER_STATS (3), PS_DRRSEQ_STATS (5), PS_FLOW_STATS (2), PS_SHAPER_STATS (4), _gqos_ps_component_stats, ntddpsch/PPS_COMPONENT_STATS, ntddpsch/PS_COMPONENT_STATS, qos.ps_component_stats'
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
req.typenames: PS_COMPONENT_STATS, *PPS_COMPONENT_STATS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PS_COMPONENT_STATS
 - ntddpsch/_PS_COMPONENT_STATS
 - PPS_COMPONENT_STATS
 - ntddpsch/PPS_COMPONENT_STATS
 - PS_COMPONENT_STATS
 - ntddpsch/PS_COMPONENT_STATS
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
 - PS_COMPONENT_STATS
---

# PS_COMPONENT_STATS structure


## -description

The 
<b>PS_COMPONENT_STATS</b> structure enables applications to get statistical information regarding their TC-enabled flow. This structure obtains information from GUID_QOS_STATISTICS_BUFFER GUID. This GUID actually is an array of 
<b>PS_COMPONENT_STATS</b>, with each element of that array (each 
<b>PS_COMPONENT_STATS</b> structure) containing one of the five PS_* structure types explained subsequently.

## -struct-fields

### -field Type

Indicates the type of PS_* structure contained in the <b>Stats</b> member.
					

This member must contain one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PS_ADAPTER_STATS__1_"></a><a id="ps_adapter_stats__1_"></a><dl>
<dt><b>PS_ADAPTER_STATS (1)</b></dt>
</dl>
</td>
<td width="60%">
<b>Stats</b> is a pointer to a <a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_adapter_stats">PS_ADAPTER_STATS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_FLOW_STATS__2_"></a><a id="ps_flow_stats__2_"></a><dl>
<dt><b>PS_FLOW_STATS (2)</b></dt>
</dl>
</td>
<td width="60%">
<b>Stats</b> is a pointer to a <a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_flow_stats">PS_FLOW_STATS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_CONFORMER_STATS__3_"></a><a id="ps_conformer_stats__3_"></a><dl>
<dt><b>PS_CONFORMER_STATS (3)</b></dt>
</dl>
</td>
<td width="60%">
<b>Stats</b> is a pointer to a <a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_conformer_stats">PS_CONFORMER_STATS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_SHAPER_STATS__4_"></a><a id="ps_shaper_stats__4_"></a><dl>
<dt><b>PS_SHAPER_STATS (4)</b></dt>
</dl>
</td>
<td width="60%">
<b>Stats</b> is a pointer to a <a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_shaper_stats">PS_SHAPER_STATS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_DRRSEQ_STATS__5_"></a><a id="ps_drrseq_stats__5_"></a><dl>
<dt><b>PS_DRRSEQ_STATS (5)</b></dt>
</dl>
</td>
<td width="60%">
<b>Stats</b> is a pointer to a <a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_drrseq_stats">PS_DRRSEQ_STATS</a> structure.

</td>
</tr>
</table>

### -field Length

Length of the <b>Stats</b> member, in bytes.

### -field Stats

Array of structures of the type indicated in the <b>Type</b> member.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_adapter_stats">PS_ADAPTER_STATS</a>



<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_conformer_stats">PS_CONFORMER_STATS</a>



<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_drrseq_stats">PS_DRRSEQ_STATS</a>



<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_flow_stats">PS_FLOW_STATS</a>



<a href="/windows/desktop/api/ntddpsch/ns-ntddpsch-ps_shaper_stats">PS_SHAPER_STATS</a>