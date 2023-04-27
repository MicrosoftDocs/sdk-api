---
UID: NS:fwpmtypes.FWPM_SUBLAYER_CHANGE0_
title: FWPM_SUBLAYER_CHANGE0 (fwpmtypes.h)
description: Change notification dispatched to subscribers. (FWPM_SUBLAYER_CHANGE0)
helpviewer_keywords: ["FWPM_SUBLAYER_CHANGE0","FWPM_SUBLAYER_CHANGE0 structure [Filtering]","fwp.fwpm_sublayer_change0_struct","fwpmtypes/FWPM_SUBLAYER_CHANGE0"]
old-location: fwp\fwpm_sublayer_change0_struct.htm
tech.root: fwp
ms.assetid: f01593aa-e7b1-42f1-b523-2f9e6d6b631b
ms.date: 12/05/2018
ms.keywords: FWPM_SUBLAYER_CHANGE0, FWPM_SUBLAYER_CHANGE0 structure [Filtering], fwp.fwpm_sublayer_change0_struct, fwpmtypes/FWPM_SUBLAYER_CHANGE0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_SUBLAYER_CHANGE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_SUBLAYER_CHANGE0_
 - fwpmtypes/FWPM_SUBLAYER_CHANGE0_
 - FWPM_SUBLAYER_CHANGE0
 - fwpmtypes/FWPM_SUBLAYER_CHANGE0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_SUBLAYER_CHANGE0
---

# FWPM_SUBLAYER_CHANGE0 structure


## -description

The <b>FWPM_SUBLAYER_CHANGE0</b> structure specifies a change notification dispatched to subscribers.

## -struct-fields

### -field changeType

Type of change as specified by [FWPM_CHANGE_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_change_type).

### -field subLayerKey

GUID of the sublayer that changed.

## -remarks

<b>FWPM_SUBLAYER_CHANGE0</b> is a specific implementation of FWPM_SUBLAYER_CHANGE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_CHANGE_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_change_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
