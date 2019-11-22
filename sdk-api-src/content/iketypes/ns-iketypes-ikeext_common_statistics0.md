---
UID: NS:iketypes.IKEEXT_COMMON_STATISTICS0_
title: IKEEXT_COMMON_STATISTICS0 (iketypes.h)

description: Various statistics common to IKE and Authip.
old-location: fwp\ikeext_common_statistics0.htm
tech.root: fwp
ms.assetid: a53ef735-3223-4ff5-9b2a-d40ab0f53570

ms.date: 12/05/2018
ms.keywords: IKEEXT_COMMON_STATISTICS0, IKEEXT_COMMON_STATISTICS0 structure [Filtering], fwp.ikeext_common_statistics0, iketypes/IKEEXT_COMMON_STATISTICS0
ms.topic: struct
f1_keywords: 
 - "iketypes/IKEEXT_COMMON_STATISTICS0"
dev_langs:
 - c++
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
 - IKEEXT_COMMON_STATISTICS0
targetos: Windows
req.typenames: IKEEXT_COMMON_STATISTICS0
req.redist: 
ms.custom: 19H1
---

# IKEEXT_COMMON_STATISTICS0 structure


## -description


The <b>IKEEXT_COMMON_STATISTICS0</b> structure contains various statistics common to IKE and Authip.
<div class="alert"><b>Note</b>  <b>IKEEXT_COMMON_STATISTICS0</b> is the specific implementation of IKEEXT_COMMON_STATISTICS used in Windows Vista. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_common_statistics1_">IKEEXT_COMMON_STATISTICS1</a> is available.</div><div> </div>

## -struct-fields




### -field v4Statistics

IPv4 common statistics.

See <a href="https://docs.microsoft.com/windows/win32/api/iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0">IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0</a> for more information.


### -field v6Statistics

IPv6 common statistics.

See <a href="https://docs.microsoft.com/windows/win32/api/iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0">IKEEXT_IP_VERSION_SPECIFIC_COMMON_STATISTICS0</a> for more information.


### -field totalPacketsReceived

Total number of packets received.


### -field totalInvalidPacketsReceived

Total number of invalid packets received.


### -field currentQueuedWorkitems

Current number of work items that are queued and waiting to be processed.

