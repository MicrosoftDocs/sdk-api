---
UID: NS:ipsectypes.IPSEC_STATISTICS0_
title: IPSEC_STATISTICS0 (ipsectypes.h)
author: windows-sdk-content
description: Is the top-level of the IPsec statistics structures.
old-location: fwp\ipsec_statistics0_struct.htm
tech.root: fwp
ms.assetid: 05873d6d-9e0c-4d3e-9b4d-7831e29e2942
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPSEC_STATISTICS0, IPSEC_STATISTICS0 structure [Filtering], fwp.ipsec_statistics0_struct, ipsectypes/IPSEC_STATISTICS0
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_STATISTICS0
product: Windows
targetos: Windows
req.typenames: IPSEC_STATISTICS0
req.redist: 
---

# IPSEC_STATISTICS0 structure


## -description


The <b>IPSEC_STATISTICS0</b> structure is the  top-level of the IPsec statistics structures.
<div class="alert"><b>Note</b>  <b>IPSEC_STATISTICS0</b> is the specific implementation of IPSEC_STATISTICS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/d61d8eb5-1b0b-419e-a248-58541db8906b">IPSEC_STATISTICS1</a> is available.</div><div> </div>

## -struct-fields




### -field aggregateSaStatistics


<a href="https://msdn.microsoft.com/en-us/library/Aa365913(v=VS.85).aspx">IPSEC_AGGREGATE_SA_STATISTICS0</a> structure containing IPsec aggregate SA statistics.


### -field espDropPacketStatistics


<a href="https://msdn.microsoft.com/en-us/library/Aa366300(v=VS.85).aspx">IPSEC_ESP_DROP_PACKET_STATISTICS0</a> structure containing IPsec ESP drop packet statistics.


### -field ahDropPacketStatistics


<a href="https://msdn.microsoft.com/en-us/library/Aa366188(v=VS.85).aspx">IPSEC_AH_DROP_PACKET_STATISTICS0</a> structure containing IPsec AH drop packet statistics.


### -field aggregateDropPacketStatistics


<a href="https://msdn.microsoft.com/en-us/library/Aa365911(v=VS.85).aspx">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0</a> structure containing IPsec aggregate drop packet statistics.


### -field inboundTrafficStatistics


<a href="https://msdn.microsoft.com/70f67966-0ced-49a7-9d27-6976ee0bd89c">IPSEC_TRAFFIC_STATISTICS0</a> structure containing IPsec inbound traffic statistics.


### -field outboundTrafficStatistics


<a href="https://msdn.microsoft.com/70f67966-0ced-49a7-9d27-6976ee0bd89c">IPSEC_TRAFFIC_STATISTICS0</a> structure containing IPsec outbound traffic statistics.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa365911(v=VS.85).aspx">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa365913(v=VS.85).aspx">IPSEC_AGGREGATE_SA_STATISTICS0</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa366188(v=VS.85).aspx">IPSEC_AH_DROP_PACKET_STATISTICS0</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa366300(v=VS.85).aspx">IPSEC_ESP_DROP_PACKET_STATISTICS0</a>



<a href="https://msdn.microsoft.com/70f67966-0ced-49a7-9d27-6976ee0bd89c">IPSEC_TRAFFIC_STATISTICS0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

