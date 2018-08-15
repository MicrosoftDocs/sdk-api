---
UID: NS:ntddpsch._PS_SHAPER_STATS
title: "_PS_SHAPER_STATS"
author: windows-sdk-content
description: The PS_SHAPER_STATS structure provides statistical packet shaper information about the computer's packet shaper component. Note that the PS_SHAPER_STATS structure is used in conjunction with the PS_COMPONENT_STATS structure.
old-location: qos\ps_shaper_stats.htm
old-project: qos
ms.assetid: fd2ef45d-154a-47b0-ba40-a823f9dd6dce
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PPS_SHAPER_STATS, PPS_SHAPER_STATS, PPS_SHAPER_STATS structure pointer [QOS], PS_SHAPER_STATS, PS_SHAPER_STATS structure [QOS], _PS_SHAPER_STATS, _gqos_ps_shaper_stats, ntddpsch/PPS_SHAPER_STATS, ntddpsch/PS_SHAPER_STATS, qos.ps_shaper_stats"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntddpsch.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PS_SHAPER_STATS, *PPS_SHAPER_STATS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntddpsch.h
api_name:
 - PS_SHAPER_STATS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _PS_SHAPER_STATS structure


## -description


The 
<b>PS_SHAPER_STATS</b> structure provides statistical packet shaper information about the computer's packet shaper component. Note that the 
<b>PS_SHAPER_STATS</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/6263d80a-5486-4748-b3a7-4c9d9bb2162f">PS_COMPONENT_STATS</a> structure.


## -struct-fields




### -field MaxPacketsInShaper

Maximum number of packets that have been in the packet shaper for the flow or interface.


### -field AveragePacketsInShaper

Average number of packets that have been in the packet shaper for the flow or interface.


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/6263d80a-5486-4748-b3a7-4c9d9bb2162f">PS_COMPONENT_STATS</a>
 

 

