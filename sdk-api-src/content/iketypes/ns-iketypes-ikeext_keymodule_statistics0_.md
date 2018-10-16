---
UID: NS:iketypes.IKEEXT_KEYMODULE_STATISTICS0_
title: IKEEXT_KEYMODULE_STATISTICS0_
author: windows-sdk-content
description: Contains various statistics specific to the keying module.
old-location: fwp\ikeext_keymodule_statistics0.htm
tech.root: fwp
ms.assetid: 87dca500-bf57-463a-a6de-db270430ae29
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IKEEXT_KEYMODULE_STATISTICS0, IKEEXT_KEYMODULE_STATISTICS0 structure [Filtering], IKEEXT_KEYMODULE_STATISTICS0_, fwp.ikeext_keymodule_statistics0, iketypes/IKEEXT_KEYMODULE_STATISTICS0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
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
 - Iketypes.h
api_name:
 - IKEEXT_KEYMODULE_STATISTICS0
product: Windows
targetos: Windows
req.typenames: IKEEXT_KEYMODULE_STATISTICS0
req.redist: 
---

# IKEEXT_KEYMODULE_STATISTICS0_ structure


## -description


The <b>IKEEXT_KEYMODULE_STATISTICS0</b> structure contains various statistics specific to the keying module.
<div class="alert"><b>Note</b>  <b>IKEEXT_KEYMODULE_STATISTICS0</b> is the specific implementation of IKEEXT_KEYMODULE_STATISTICS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/3b5fdf04-e3a6-4658-a53d-66928b5682f5">IKEEXT_KEYMODULE_STATISTICS1</a> is available.</div><div> </div>

## -struct-fields




### -field v4Statistics

IPv4 common statistics.

See <a href="https://msdn.microsoft.com/5b5bb140-ca44-4a46-bb96-aba0b499e94f">IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0</a> for more information.


### -field v6Statistics

IPv6 common statistics.

See <a href="https://msdn.microsoft.com/5b5bb140-ca44-4a46-bb96-aba0b499e94f">IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS0</a> for more information.


### -field errorFrequencyTable

Table containing the frequencies of various IKE Win32 error codes encountered during negotiations. The error codes range from ERROR_IPSEC_IKE_NEG_STATUS_BEGIN to ERROR_IPSEC_IKE_NEG_STATUS_END. 

The table size, IKEEXT_ERROR_CODE_COUNT, is 84 (ERROR_IPSEC_IKE_NEG_STATUS_END - ERROR_IPSEC_IKE_NEG_STATUS_BEGIN).


### -field mainModeNegotiationTime

Current Main Mode negotiation time.


### -field quickModeNegotiationTime

Current Quick Mode negotiation time.


### -field extendedModeNegotiationTime

Current Extended Mode negotiation time.  This member is applicable for Authip only.

