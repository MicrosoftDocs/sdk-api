---
UID: NS:iketypes.IKEEXT_KEYMODULE_STATISTICS1_
title: IKEEXT_KEYMODULE_STATISTICS1 (iketypes.h)
description: Contains various statistics specific to the keying module. (IKEEXT_KEYMODULE_STATISTICS1)
helpviewer_keywords: ["IKEEXT_KEYMODULE_STATISTICS1","IKEEXT_KEYMODULE_STATISTICS1 structure [Filtering]","fwp.ikeext_keymodule_statistics1","iketypes/IKEEXT_KEYMODULE_STATISTICS1"]
old-location: fwp\ikeext_keymodule_statistics1.htm
tech.root: fwp
ms.assetid: 3b5fdf04-e3a6-4658-a53d-66928b5682f5
ms.date: 12/05/2018
ms.keywords: IKEEXT_KEYMODULE_STATISTICS1, IKEEXT_KEYMODULE_STATISTICS1 structure [Filtering], fwp.ikeext_keymodule_statistics1, iketypes/IKEEXT_KEYMODULE_STATISTICS1
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: IKEEXT_KEYMODULE_STATISTICS1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_KEYMODULE_STATISTICS1_
 - iketypes/IKEEXT_KEYMODULE_STATISTICS1_
 - IKEEXT_KEYMODULE_STATISTICS1
 - iketypes/IKEEXT_KEYMODULE_STATISTICS1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_KEYMODULE_STATISTICS1
---

# IKEEXT_KEYMODULE_STATISTICS1 structure


## -description

The <b>IKEEXT_KEYMODULE_STATISTICS1</b> structure contains various statistics specific to the keying module.
[IKEEXT_KEYMODULE_STATISTICS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_keymodule_statistics0) is available.</div><div> </div>

## -struct-fields

### -field v4Statistics

IPv4 common statistics.

See <a href="/windows/win32/api/iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1">IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1</a> for more information.

### -field v6Statistics

IPv6 common statistics.

See <a href="/windows/win32/api/iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1">IKEEXT_IP_VERSION_SPECIFIC_KEYMODULE_STATISTICS1</a> for more information.

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

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
