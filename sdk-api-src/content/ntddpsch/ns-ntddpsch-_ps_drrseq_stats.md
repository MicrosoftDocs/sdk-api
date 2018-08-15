---
UID: NS:ntddpsch._PS_DRRSEQ_STATS
title: "_PS_DRRSEQ_STATS"
author: windows-sdk-content
description: The PS_DRRSEQ_STATS structure provides network interface card (NIC) and packet sequencer&#8211;packet shaper statistics. Note that the PS_DRRSEQ_STATS structure is used in conjunction with the PS_COMPONENT_STATS structure.
old-location: qos\ps_drrseq_stats.htm
old-project: qos
ms.assetid: c8d5bf61-5a19-4bbd-ae4c-0502b6803191
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PPS_DRRSEQ_STATS, PPS_DRRSEQ_STATS, PPS_DRRSEQ_STATS structure pointer [QOS], PS_DRRSEQ_STATS, PS_DRRSEQ_STATS structure [QOS], _PS_DRRSEQ_STATS, _gqos_ps_drrseq_stats, ntddpsch/PPS_DRRSEQ_STATS, ntddpsch/PS_DRRSEQ_STATS, qos.ps_drrseq_stats"
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
req.typenames: PS_DRRSEQ_STATS, *PPS_DRRSEQ_STATS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntddpsch.h
api_name:
 - PS_DRRSEQ_STATS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _PS_DRRSEQ_STATS structure


## -description


The 
<b>PS_DRRSEQ_STATS</b> structure provides network interface card (NIC) and packet sequencer–packet shaper statistics. Note that the 
<b>PS_DRRSEQ_STATS</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/6263d80a-5486-4748-b3a7-4c9d9bb2162f">PS_COMPONENT_STATS</a> structure.


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




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/6263d80a-5486-4748-b3a7-4c9d9bb2162f">PS_COMPONENT_STATS</a>
 

 

