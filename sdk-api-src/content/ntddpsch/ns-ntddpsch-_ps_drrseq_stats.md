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
 

 

