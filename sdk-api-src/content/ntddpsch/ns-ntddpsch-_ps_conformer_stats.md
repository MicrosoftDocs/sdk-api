---
UID: NS:ntddpsch._PS_CONFORMER_STATS
title: "_PS_CONFORMER_STATS"
author: windows-driver-content
description: The PS_CONFORMER_STATS structure provides statistical packet shaper information about a particular flow. Note that the PS_CONFORMER_STATS structure is used in conjunction with the PS_COMPONENT_STATS structure.
old-location: qos\ps_conformer_stats.htm
old-project: QOS
ms.assetid: 709274fe-de56-4f86-9002-71f0ee333ace
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*PPS_CONFORMER_STATS, PPS_CONFORMER_STATS, PPS_CONFORMER_STATS structure pointer [QOS], PS_CONFORMER_STATS, PS_CONFORMER_STATS structure [QOS], _PS_CONFORMER_STATS, _gqos_ps_conformer_stats, ntddpsch/PPS_CONFORMER_STATS, ntddpsch/PS_CONFORMER_STATS, qos.ps_conformer_stats"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: PS_CONFORMER_STATS, *PPS_CONFORMER_STATS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntddpsch.h
api_name:
-	PS_CONFORMER_STATS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _PS_CONFORMER_STATS structure


## -description


The 
<b>PS_CONFORMER_STATS</b> structure provides statistical packet shaper information about a particular flow. Note that the 
<b>PS_CONFORMER_STATS</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/6263d80a-5486-4748-b3a7-4c9d9bb2162f">PS_COMPONENT_STATS</a> structure.


## -struct-fields




### -field NonconformingPacketsScheduled

Number of nonconforming packets that have been scheduled on the flow or interface.


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/6263d80a-5486-4748-b3a7-4c9d9bb2162f">PS_COMPONENT_STATS</a>
 

 

