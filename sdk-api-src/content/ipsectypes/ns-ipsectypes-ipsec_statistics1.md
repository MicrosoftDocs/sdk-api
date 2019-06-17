---
UID: NS:ipsectypes.IPSEC_STATISTICS1_
title: IPSEC_STATISTICS1 (ipsectypes.h)
author: windows-sdk-content
description: Is the top-level of the IPsec statistics structures.
old-location: fwp\ipsec_statistics1_struct.htm
tech.root: fwp
ms.assetid: d61d8eb5-1b0b-419e-a248-58541db8906b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPSEC_STATISTICS1, IPSEC_STATISTICS1 structure [Filtering], fwp.ipsec_statistics1_struct, ipsectypes/IPSEC_STATISTICS1
ms.topic: struct
f1_keywords: ["ipsectypes/IPSEC_STATISTICS1"]
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
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
 - Ipsectypes.h
api_name:
 - IPSEC_STATISTICS1
product: Windows
targetos: Windows
req.typenames: IPSEC_STATISTICS1
req.redist: 
ms.custom: 19H1
---

# IPSEC_STATISTICS1 structure


## -description


The <b>IPSEC_STATISTICS1</b> structure is the  top-level of the IPsec statistics structures.
<div class="alert"><b>Note</b>  <b>IPSEC_STATISTICS1</b> is the specific implementation of IPSEC_STATISTICS used in Windows 7 and later. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_statistics0_">IPSEC_STATISTICS0</a> is available.</div><div> </div>

## -struct-fields




### -field aggregateSaStatistics


<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0_">IPSEC_AGGREGATE_SA_STATISTICS0</a> structure containing IPsec aggregate SA statistics.


### -field espDropPacketStatistics


<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0_">IPSEC_ESP_DROP_PACKET_STATISTICS0</a> structure containing IPsec ESP drop packet statistics.


### -field ahDropPacketStatistics


<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0_">IPSEC_AH_DROP_PACKET_STATISTICS0</a> structure containing IPsec AH drop packet statistics.


### -field aggregateDropPacketStatistics


<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1_">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS1</a> structure containing IPsec aggregate drop packet statistics.


### -field inboundTrafficStatistics


<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1_">IPSEC_TRAFFIC_STATISTICS1</a> structure containing IPsec inbound traffic statistics.


### -field outboundTrafficStatistics


<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1_">IPSEC_TRAFFIC_STATISTICS1</a> structure containing IPsec outbound traffic statistics.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1_">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0_">IPSEC_AGGREGATE_SA_STATISTICS0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0_">IPSEC_AH_DROP_PACKET_STATISTICS0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0_">IPSEC_ESP_DROP_PACKET_STATISTICS0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1_">IPSEC_TRAFFIC_STATISTICS1</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

