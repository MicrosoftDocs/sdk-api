---
UID: NS:ntddpsch._PS_FLOW_STATS
title: "_PS_FLOW_STATS"
author: windows-sdk-content
description: The PS_FLOW_STATS structure provides statistical packet shaper information about a particular flow. Note that the PS_FLOW_STATS structure is used in conjunction with the PS_COMPONENT_STATS structure.
old-location: qos\ps_flow_stats.htm
tech.root: QOS
ms.assetid: 1d40c247-9e61-4f8b-85f9-eddc90727a17
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PPS_FLOW_STATS, PPS_FLOW_STATS, PPS_FLOW_STATS structure pointer [QOS], PS_FLOW_STATS, PS_FLOW_STATS structure [QOS], _PS_FLOW_STATS, _gqos_ps_flow_stats, ntddpsch/PPS_FLOW_STATS, ntddpsch/PS_FLOW_STATS, qos.ps_flow_stats"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntddpsch.h
api_name:
 - PS_FLOW_STATS
product: Windows
targetos: Windows
req.typenames: PS_FLOW_STATS, *PPS_FLOW_STATS
req.redist: 
---

# _PS_FLOW_STATS structure


## -description


The 
<b>PS_FLOW_STATS</b> structure provides statistical packet shaper information about a particular flow. Note that the 
<b>PS_FLOW_STATS</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/6263d80a-5486-4748-b3a7-4c9d9bb2162f">PS_COMPONENT_STATS</a> structure.


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




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/6263d80a-5486-4748-b3a7-4c9d9bb2162f">PS_COMPONENT_STATS</a>
 

 

