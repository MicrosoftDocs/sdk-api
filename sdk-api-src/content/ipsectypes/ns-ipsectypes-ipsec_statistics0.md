---
UID: NS:ipsectypes.IPSEC_STATISTICS0_
title: IPSEC_STATISTICS0 (ipsectypes.h)
description: Is the top-level of the IPsec statistics structures. (IPSEC_STATISTICS0)
helpviewer_keywords: ["IPSEC_STATISTICS0","IPSEC_STATISTICS0 structure [Filtering]","fwp.ipsec_statistics0_struct","ipsectypes/IPSEC_STATISTICS0"]
old-location: fwp\ipsec_statistics0_struct.htm
tech.root: fwp
ms.assetid: 05873d6d-9e0c-4d3e-9b4d-7831e29e2942
ms.date: 12/05/2018
ms.keywords: IPSEC_STATISTICS0, IPSEC_STATISTICS0 structure [Filtering], fwp.ipsec_statistics0_struct, ipsectypes/IPSEC_STATISTICS0
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: IPSEC_STATISTICS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_STATISTICS0_
 - ipsectypes/IPSEC_STATISTICS0_
 - IPSEC_STATISTICS0
 - ipsectypes/IPSEC_STATISTICS0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_STATISTICS0
---

# IPSEC_STATISTICS0 structure


## -description

The <b>IPSEC_STATISTICS0</b> structure is the  top-level of the IPsec statistics structures.
[IPSEC_STATISTICS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_statistics1) is available.</div><div> </div>

## -struct-fields

### -field aggregateSaStatistics

<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0">IPSEC_AGGREGATE_SA_STATISTICS0</a> structure containing IPsec aggregate SA statistics.

### -field espDropPacketStatistics

<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0">IPSEC_ESP_DROP_PACKET_STATISTICS0</a> structure containing IPsec ESP drop packet statistics.

### -field ahDropPacketStatistics

<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0">IPSEC_AH_DROP_PACKET_STATISTICS0</a> structure containing IPsec AH drop packet statistics.

### -field aggregateDropPacketStatistics

<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0</a> structure containing IPsec aggregate drop packet statistics.

### -field inboundTrafficStatistics

[IPSEC_TRAFFIC_STATISTICS0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0) structure containing IPsec inbound traffic statistics.

### -field outboundTrafficStatistics

[IPSEC_TRAFFIC_STATISTICS0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0) structure containing IPsec outbound traffic statistics.

## -see-also

<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0</a>



<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0">IPSEC_AGGREGATE_SA_STATISTICS0</a>



<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0">IPSEC_AH_DROP_PACKET_STATISTICS0</a>



<a href="/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0">IPSEC_ESP_DROP_PACKET_STATISTICS0</a>



[IPSEC_TRAFFIC_STATISTICS0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
