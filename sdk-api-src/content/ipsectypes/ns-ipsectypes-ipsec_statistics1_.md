---
UID: NS:ipsectypes.IPSEC_STATISTICS1_
title: IPSEC_STATISTICS1_
author: windows-sdk-content
description: Is the top-level of the IPsec statistics structures.
old-location: fwp\ipsec_statistics1_struct.htm
tech.root: fwp
ms.assetid: d61d8eb5-1b0b-419e-a248-58541db8906b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPSEC_STATISTICS1, IPSEC_STATISTICS1 structure [Filtering], IPSEC_STATISTICS1_, fwp.ipsec_statistics1_struct, ipsectypes/IPSEC_STATISTICS1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 

 

