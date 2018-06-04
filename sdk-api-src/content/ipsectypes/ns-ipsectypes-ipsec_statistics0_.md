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

# IPSEC_STATISTICS0_ structure


## -description


The <b>IPSEC_STATISTICS0</b> structure is the  top-level of the IPsec statistics structures.
<div class="alert"><b>Note</b>  <b>IPSEC_STATISTICS0</b> is the specific implementation of IPSEC_STATISTICS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/d61d8eb5-1b0b-419e-a248-58541db8906b">IPSEC_STATISTICS1</a> is available.</div><div> </div>

## -struct-fields




### -field aggregateSaStatistics


<a href="https://msdn.microsoft.com/f0318061-40f9-4380-9681-34db70659c49">IPSEC_AGGREGATE_SA_STATISTICS0</a> structure containing IPsec aggregate SA statistics.


### -field espDropPacketStatistics


<a href="https://msdn.microsoft.com/d31ac463-8265-40c6-bd68-9f3ade35eb34">IPSEC_ESP_DROP_PACKET_STATISTICS0</a> structure containing IPsec ESP drop packet statistics.


### -field ahDropPacketStatistics


<a href="https://msdn.microsoft.com/dca4d313-fb88-475f-adee-7c42abe550d5">IPSEC_AH_DROP_PACKET_STATISTICS0</a> structure containing IPsec AH drop packet statistics.


### -field aggregateDropPacketStatistics


<a href="https://msdn.microsoft.com/f7c955af-97ec-4c27-a9de-d1498398608e">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0</a> structure containing IPsec aggregate drop packet statistics.


### -field inboundTrafficStatistics


<a href="https://msdn.microsoft.com/70f67966-0ced-49a7-9d27-6976ee0bd89c">IPSEC_TRAFFIC_STATISTICS0</a> structure containing IPsec inbound traffic statistics.


### -field outboundTrafficStatistics


<a href="https://msdn.microsoft.com/70f67966-0ced-49a7-9d27-6976ee0bd89c">IPSEC_TRAFFIC_STATISTICS0</a> structure containing IPsec outbound traffic statistics.


## -see-also




<a href="https://msdn.microsoft.com/f7c955af-97ec-4c27-a9de-d1498398608e">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0</a>



<a href="https://msdn.microsoft.com/f0318061-40f9-4380-9681-34db70659c49">IPSEC_AGGREGATE_SA_STATISTICS0</a>



<a href="https://msdn.microsoft.com/dca4d313-fb88-475f-adee-7c42abe550d5">IPSEC_AH_DROP_PACKET_STATISTICS0</a>



<a href="https://msdn.microsoft.com/d31ac463-8265-40c6-bd68-9f3ade35eb34">IPSEC_ESP_DROP_PACKET_STATISTICS0</a>



<a href="https://msdn.microsoft.com/70f67966-0ced-49a7-9d27-6976ee0bd89c">IPSEC_TRAFFIC_STATISTICS0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

