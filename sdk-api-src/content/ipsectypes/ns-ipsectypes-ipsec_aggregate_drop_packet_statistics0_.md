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

# IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0_ structure


## -description


The <b>IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0</b> structure stores aggregate IPsec kernel packet drop statistics.<div class="alert"><b>Note</b>  <b>IPSEC_AGGREGATE_DROP_PACKET_STATISTICS0</b> is the specific implementation of IPSEC_AGGREGATE_DROP_PACKET_STATISTICS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/8ee7150e-ac6e-4f8e-99af-1b92b4e54615">IPSEC_AGGREGATE_DROP_PACKET_STATISTICS1</a> is available.</div>
<div> </div>



## -struct-fields




### -field invalidSpisOnInbound

Number of invalid SPIs on inbound.


### -field decryptionFailuresOnInbound

Number of decryption failures on inbound.


### -field authenticationFailuresOnInbound

Number of authentication failures on inbound.


### -field udpEspValidationFailuresOnInbound

Number of UDP ESP validation failures on inbound.


### -field replayCheckFailuresOnInbound

Number of replay check failures on inbound.


### -field invalidClearTextInbound

Number of invalid clear text instances on inbound.


### -field saNotInitializedOnInbound

Number of inbound drops for packets received on SAs that were not fully initialized.


### -field receiveOverIncorrectSaInbound

Number of inbound drops for packets received on SAs whose characteristics did not match the packet.


### -field secureReceivesNotMatchingFilters

Number of inbound IPsec secured packets that did not match any inbound IPsec transport layer filter.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

