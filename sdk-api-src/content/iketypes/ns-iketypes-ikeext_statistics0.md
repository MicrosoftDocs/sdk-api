---
UID: NS:iketypes.IKEEXT_STATISTICS0_
title: IKEEXT_STATISTICS0 (iketypes.h)
author: windows-sdk-content
description: Stores various IKE/AuthIP statistics.
old-location: fwp\ikeext_statistics0.htm
tech.root: fwp
ms.assetid: aefacc39-92a5-4d73-ac3c-0b5bf1407a90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKEEXT_STATISTICS0, IKEEXT_STATISTICS0 structure [Filtering], fwp.ikeext_statistics0, iketypes/IKEEXT_STATISTICS0
ms.topic: struct
f1_keywords: 
 - "iketypes/IKEEXT_STATISTICS0"
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
 - IKEEXT_STATISTICS0
product: Windows
targetos: Windows
req.typenames: IKEEXT_STATISTICS0
req.redist: 
ms.custom: 19H1
---

# IKEEXT_STATISTICS0 structure


## -description


The <b>IKEEXT_STATISTICS0</b> structure stores various IKE/AuthIP statistics.
<div class="alert"><b>Note</b>  <b>IKEEXT_STATISTICS0</b> is the specific implementation of IKEEXT_STATISTICS used in Windows Vista. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_statistics1_">IKEEXT_STATISTICS1</a> is available.</div><div> </div>

## -struct-fields




### -field ikeStatistics

Statistics specific to IKE.

See <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_keymodule_statistics0_">IKEEXT_KEYMODULE_STATISTICS0</a> for more information.


### -field authipStatistics

Statistics specific to AuthIP.

See <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_keymodule_statistics0_">IKEEXT_KEYMODULE_STATISTICS0</a> for more information.


### -field commonStatistics

Statistics common to IKE and AuthIP.

See <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_common_statistics0_">IKEEXT_COMMON_STATISTICS0</a> for more information.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_keymodule_statistics0_">IKEEXT_KEYMODULE_STATISTICS0</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

