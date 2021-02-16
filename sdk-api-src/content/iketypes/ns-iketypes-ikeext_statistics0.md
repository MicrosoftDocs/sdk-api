---
UID: NS:iketypes.IKEEXT_STATISTICS0_
title: IKEEXT_STATISTICS0 (iketypes.h)
description: Stores various IKE/AuthIP statistics.
helpviewer_keywords: ["IKEEXT_STATISTICS0","IKEEXT_STATISTICS0 structure [Filtering]","fwp.ikeext_statistics0","iketypes/IKEEXT_STATISTICS0"]
old-location: fwp\ikeext_statistics0.htm
tech.root: fwp
ms.assetid: aefacc39-92a5-4d73-ac3c-0b5bf1407a90
ms.date: 12/05/2018
ms.keywords: IKEEXT_STATISTICS0, IKEEXT_STATISTICS0 structure [Filtering], fwp.ikeext_statistics0, iketypes/IKEEXT_STATISTICS0
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
targetos: Windows
req.typenames: IKEEXT_STATISTICS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_STATISTICS0_
 - iketypes/IKEEXT_STATISTICS0_
 - IKEEXT_STATISTICS0
 - iketypes/IKEEXT_STATISTICS0
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
 - IKEEXT_STATISTICS0
---

# IKEEXT_STATISTICS0 structure


## -description

The <b>IKEEXT_STATISTICS0</b> structure stores various IKE/AuthIP statistics.
[IKEEXT_STATISTICS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_statistics1) is available.</div><div> </div>

## -struct-fields

### -field ikeStatistics

Statistics specific to IKE.

See [IKEEXT_KEYMODULE_STATISTICS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_keymodule_statistics0) for more information.

### -field authipStatistics

Statistics specific to AuthIP.

See [IKEEXT_KEYMODULE_STATISTICS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_keymodule_statistics0) for more information.

### -field commonStatistics

Statistics common to IKE and AuthIP.

See [IKEEXT_COMMON_STATISTICS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_common_statistics0) for more information.

## -see-also

[IKEEXT_KEYMODULE_STATISTICS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_keymodule_statistics0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>