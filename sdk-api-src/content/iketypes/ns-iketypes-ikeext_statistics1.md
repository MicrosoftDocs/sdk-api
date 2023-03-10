---
UID: NS:iketypes.IKEEXT_STATISTICS1_
title: IKEEXT_STATISTICS1 (iketypes.h)
description: Stores various IKE, AuthIP, and IKEv2 statistics.
helpviewer_keywords: ["IKEEXT_STATISTICS1","IKEEXT_STATISTICS1 structure [Filtering]","fwp.ikeext_statistics1","iketypes/IKEEXT_STATISTICS1"]
old-location: fwp\ikeext_statistics1.htm
tech.root: fwp
ms.assetid: 73c36ea1-d009-4724-8b1c-54503ad57e4d
ms.date: 12/05/2018
ms.keywords: IKEEXT_STATISTICS1, IKEEXT_STATISTICS1 structure [Filtering], fwp.ikeext_statistics1, iketypes/IKEEXT_STATISTICS1
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
req.typenames: IKEEXT_STATISTICS1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_STATISTICS1_
 - iketypes/IKEEXT_STATISTICS1_
 - IKEEXT_STATISTICS1
 - iketypes/IKEEXT_STATISTICS1
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
 - IKEEXT_STATISTICS1
---

## -description

The [IKEEXT_STATISTICS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_statistics0) structure stores various IKE, AuthIP, and IKEv2 statistics.
[IKEEXT_STATISTICS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_statistics0) is the specific implementation of IKEEXT_STATISTICS used in Windows 7 and later. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <b>IKEEXT_STATISTICS0</b> is available.

## -struct-fields

### -field ikeStatistics

Statistics specific to IKE.

See [IKEEXT_KEYMODULE_STATISTICS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_keymodule_statistics1) for more information.

### -field authipStatistics

Statistics specific to AuthIP.

See [IKEEXT_KEYMODULE_STATISTICS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_keymodule_statistics1) for more information.

### -field ikeV2Statistics

Statistics specific to IKEv2.

See [IKEEXT_KEYMODULE_STATISTICS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_keymodule_statistics1) for more information.

### -field commonStatistics

Statistics common to IKE, AuthIP, and IKEv2.

See [IKEEXT_COMMON_STATISTICS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_common_statistics1) for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>