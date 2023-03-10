---
UID: NS:fwpmtypes.FWPM_FILTER_CHANGE0_
title: FWPM_FILTER_CHANGE0 (fwpmtypes.h)
description: Stores change notification dispatched to subscribers.
helpviewer_keywords: ["FWPM_FILTER_CHANGE0","FWPM_FILTER_CHANGE0 structure [Filtering]","fwp.fwpm_filter_change0_struct","fwpmtypes/FWPM_FILTER_CHANGE0"]
old-location: fwp\fwpm_filter_change0_struct.htm
tech.root: fwp
ms.assetid: 01c58002-5506-4e2a-ae85-30b16aad2dd6
ms.date: 12/05/2018
ms.keywords: FWPM_FILTER_CHANGE0, FWPM_FILTER_CHANGE0 structure [Filtering], fwp.fwpm_filter_change0_struct, fwpmtypes/FWPM_FILTER_CHANGE0
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
req.typenames: FWPM_FILTER_CHANGE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_FILTER_CHANGE0_
 - fwpmtypes/FWPM_FILTER_CHANGE0_
 - FWPM_FILTER_CHANGE0
 - fwpmtypes/FWPM_FILTER_CHANGE0
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
 - FWPM_FILTER_CHANGE0
---

# FWPM_FILTER_CHANGE0 structure


## -description

The <b>FWPM_FILTER_CHANGE0</b> structure stores change notification dispatched to subscribers.

## -struct-fields

### -field changeType

A [FWPM_CHANGE_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_change_type) value that specifies the type of change notification to be dispatched.

### -field filterKey

GUID of the filter that changed.

### -field filterId

LUID of the filter that changed.

## -remarks

<b>FWPM_FILTER_CHANGE0</b> is a specific implementation of FWPM_FILTER_CHANGE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_CHANGE_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_change_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>