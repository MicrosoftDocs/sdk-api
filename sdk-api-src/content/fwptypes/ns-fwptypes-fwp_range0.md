---
UID: NS:fwptypes.FWP_RANGE0_
title: FWP_RANGE0 (fwptypes.h)
description: Specifies a range of values.
helpviewer_keywords: ["FWP_RANGE0","FWP_RANGE0 structure [Filtering]","fwp.fwp_range0","fwptypes/FWP_RANGE0"]
old-location: fwp\fwp_range0.htm
tech.root: fwp
ms.assetid: 191ec0e4-2489-4f6f-80c5-8feec83d69c2
ms.date: 12/05/2018
ms.keywords: FWP_RANGE0, FWP_RANGE0 structure [Filtering], fwp.fwp_range0, fwptypes/FWP_RANGE0
req.header: fwptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwptypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWP_RANGE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWP_RANGE0_
 - fwptypes/FWP_RANGE0_
 - FWP_RANGE0
 - fwptypes/FWP_RANGE0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwptypes.h
api_name:
 - FWP_RANGE0
---

# FWP_RANGE0 structure


## -description

The <b>FWP_RANGE0</b> structure specifies a range of values.

## -struct-fields

### -field valueLow

Low value of the range.

See [FWP_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0) for more information.

### -field valueHigh

High value of the range.

See [FWP_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0) for more information.

## -remarks

The elements <b>valueLow</b> and <b>valueHigh</b> must be the same data type and 
<b>valueHigh</b> must be greater than or equal to <b>valueLow</b>. 

Ranges are always inclusive. Thus, if a value equals
<b>valueLow</b> or <b>valueHigh</b>, it is contained in the range.

<b>FWP_RANGE0</b> is a specific implementation of FWP_RANGE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWP_VALUE0](/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>