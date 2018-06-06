---
UID: NS:ipsectypes.IPSEC_ESP_DROP_PACKET_STATISTICS0_
title: IPSEC_ESP_DROP_PACKET_STATISTICS0_
author: windows-sdk-content
description: Stores ESP drop packet statistics.
old-location: fwp\ipsec_esp_drop_packet_statistics0_struct.htm
old-project: FWP
ms.assetid: d31ac463-8265-40c6-bd68-9f3ade35eb34
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IPSEC_ESP_DROP_PACKET_STATISTICS0, IPSEC_ESP_DROP_PACKET_STATISTICS0 structure [Filtering], IPSEC_ESP_DROP_PACKET_STATISTICS0_, fwp.ipsec_esp_drop_packet_statistics0_struct, ipsectypes/IPSEC_ESP_DROP_PACKET_STATISTICS0
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: IPSEC_ESP_DROP_PACKET_STATISTICS0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_ESP_DROP_PACKET_STATISTICS0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_ESP_DROP_PACKET_STATISTICS0_ structure


## -description


The <b>IPSEC_ESP_DROP_PACKET_STATISTICS0</b> structure stores ESP drop packet statistics.


## -struct-fields




### -field invalidSpisOnInbound

Number of invalid SPIs on inbound.


### -field decryptionFailuresOnInbound

Number of decryption failures on inbound.


### -field authenticationFailuresOnInbound

Number of authentication failures on inbound.


### -field replayCheckFailuresOnInbound

Number of replay check failures on inbound.


### -field saNotInitializedOnInbound

Number of inbound drops for packets received on SAs that were not fully initialized.


## -remarks



<b>IPSEC_ESP_DROP_PACKET_STATISTICS0</b> is a specific implementation of IPSEC_ESP_DROP_PACKET_STATISTICS. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

