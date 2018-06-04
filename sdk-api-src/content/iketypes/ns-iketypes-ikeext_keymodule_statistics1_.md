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

# IKEEXT_KEYMODULE_STATISTICS1_ structure


## -description


The <b>IKEEXT_KEYMODULE_STATISTICS1</b> structure contains various statistics specific to the keying module.
<div class="alert"><b>Note</b>  <b>IKEEXT_KEYMODULE_STATISTICS1</b> is the specific implementation of IKEEXT_KEYMODULE_STATISTICS used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/87dca500-bf57-463a-a6de-db270430ae29">IKEEXT_KEYMODULE_STATISTICS0</a> is available.</div><div> </div>

## -struct-fields




### -field v4Statistics

IPv4 common statistics.

See <a href="https://msdn.microsoft.com/45485729-dc02-4c59-83d7-0564e943e60b">IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1</a> for more information.


### -field v6Statistics

IPv6 common statistics.

See <a href="https://msdn.microsoft.com/45485729-dc02-4c59-83d7-0564e943e60b">IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1</a> for more information.


### -field errorFrequencyTable

Table containing the frequencies of various IKE Win32 error codes encountered during negotiations. The error codes range from ERROR_IPSEC_IKE_NEG_STATUS_BEGIN to ERROR_IPSEC_IKE_NEG_STATUS_END. 

The table size, IKEEXT_ERROR_CODE_COUNT, is 84 (ERROR_IPSEC_IKE_NEG_STATUS_END - ERROR_IPSEC_IKE_NEG_STATUS_BEGIN).


### -field mainModeNegotiationTime

Current Main Mode negotiation time.


### -field quickModeNegotiationTime

Current Quick Mode negotiation time.


### -field extendedModeNegotiationTime

Current Extended Mode negotiation time.  This member is applicable for AuthIp only.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

