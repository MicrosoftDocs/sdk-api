---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _PS_COMPONENT_STATS structure


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
<b>Stats</b> is a pointer to a <a href="https://msdn.microsoft.com/365b3987-9a7a-4c15-980d-aa39956c68c8">PS_ADAPTER_STATS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_FLOW_STATS__2_"></a><a id="ps_flow_stats__2_"></a><dl>
<dt><b>PS_FLOW_STATS (2)</b></dt>
</dl>
</td>
<td width="60%">
<b>Stats</b> is a pointer to a <a href="https://msdn.microsoft.com/1d40c247-9e61-4f8b-85f9-eddc90727a17">PS_FLOW_STATS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_CONFORMER_STATS__3_"></a><a id="ps_conformer_stats__3_"></a><dl>
<dt><b>PS_CONFORMER_STATS (3)</b></dt>
</dl>
</td>
<td width="60%">
<b>Stats</b> is a pointer to a <a href="https://msdn.microsoft.com/709274fe-de56-4f86-9002-71f0ee333ace">PS_CONFORMER_STATS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_SHAPER_STATS__4_"></a><a id="ps_shaper_stats__4_"></a><dl>
<dt><b>PS_SHAPER_STATS (4)</b></dt>
</dl>
</td>
<td width="60%">
<b>Stats</b> is a pointer to a <a href="https://msdn.microsoft.com/fd2ef45d-154a-47b0-ba40-a823f9dd6dce">PS_SHAPER_STATS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_DRRSEQ_STATS__5_"></a><a id="ps_drrseq_stats__5_"></a><dl>
<dt><b>PS_DRRSEQ_STATS (5)</b></dt>
</dl>
</td>
<td width="60%">
<b>Stats</b> is a pointer to a <a href="https://msdn.microsoft.com/c8d5bf61-5a19-4bbd-ae4c-0502b6803191">PS_DRRSEQ_STATS</a> structure.

</td>
</tr>
</table>
 


### -field Length

Length of the <b>Stats</b> member, in bytes.


### -field Stats

Array of structures of the type indicated in the <b>Type</b> member.


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/365b3987-9a7a-4c15-980d-aa39956c68c8">PS_ADAPTER_STATS</a>



<a href="https://msdn.microsoft.com/709274fe-de56-4f86-9002-71f0ee333ace">PS_CONFORMER_STATS</a>



<a href="https://msdn.microsoft.com/c8d5bf61-5a19-4bbd-ae4c-0502b6803191">PS_DRRSEQ_STATS</a>



<a href="https://msdn.microsoft.com/1d40c247-9e61-4f8b-85f9-eddc90727a17">PS_FLOW_STATS</a>



<a href="https://msdn.microsoft.com/fd2ef45d-154a-47b0-ba40-a823f9dd6dce">PS_SHAPER_STATS</a>
 

 

