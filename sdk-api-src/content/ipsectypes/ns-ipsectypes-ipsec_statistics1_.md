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

# IPSEC_STATISTICS1_ structure


## -description


The <b>IPSEC_STATISTICS1</b> structure is the  top-level of the IPsec statistics structures.
<div class="alert"><b>Note</b>  <b>IPSEC_STATISTICS1</b> is the specific implementation of IPSEC_STATISTICS used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/05873d6d-9e0c-4d3e-9b4d-7831e29e2942">IPSEC_STATISTICS0</a> is available.</div><div> </div>

## -struct-fields




### -field aggregateSaStatistics


<a href="https://msdn.microsoft.com/f0318061-40f9-4380-9681-34db70659c49">IPSEC_AGGREGATE_SA_STATISTICS0</a> structure containing IPsec aggregate SA statistics.


### -field espDropPacketStatistics


<a href="https://msdn.microsoft.com/d31ac463-8265-40c6-bd68-9f3ade35eb34">IPSEC_ESP_DROP_PACKET_STATISTICS0</a> structure containing IPsec ESP drop packet statistics.


### -field ahDropPacketStatistics


<a href="https://msdn.microsoft.com/dca4d313-fb88-475f-adee-7c42abe550d5">IPSEC_AH_DROP_PACKET_STATISTICS0</a> structure containing IPsec AH drop packet statistics.


### -field aggregateDropPacketStatistics


<a href="https://msdn.microsoft.com/8ee7150e-ac6e-4f8e-99af-1b92b4e54615">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS1</a> structure containing IPsec aggregate drop packet statistics.


### -field inboundTrafficStatistics


<a href="https://msdn.microsoft.com/3b25d98a-9216-4e74-91fc-cc8658e12d9b">IPSEC_TRAFFIC_STATISTICS1</a> structure containing IPsec inbound traffic statistics.


### -field outboundTrafficStatistics


<a href="https://msdn.microsoft.com/3b25d98a-9216-4e74-91fc-cc8658e12d9b">IPSEC_TRAFFIC_STATISTICS1</a> structure containing IPsec outbound traffic statistics.


## -see-also




<a href="https://msdn.microsoft.com/8ee7150e-ac6e-4f8e-99af-1b92b4e54615">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS1</a>



<a href="https://msdn.microsoft.com/f0318061-40f9-4380-9681-34db70659c49">IPSEC_AGGREGATE_SA_STATISTICS0</a>



<a href="https://msdn.microsoft.com/dca4d313-fb88-475f-adee-7c42abe550d5">IPSEC_AH_DROP_PACKET_STATISTICS0</a>



<a href="https://msdn.microsoft.com/d31ac463-8265-40c6-bd68-9f3ade35eb34">IPSEC_ESP_DROP_PACKET_STATISTICS0</a>



<a href="https://msdn.microsoft.com/3b25d98a-9216-4e74-91fc-cc8658e12d9b">IPSEC_TRAFFIC_STATISTICS1</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

