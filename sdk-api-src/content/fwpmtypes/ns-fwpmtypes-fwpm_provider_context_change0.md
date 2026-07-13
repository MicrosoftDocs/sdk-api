---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT_CHANGE0_
title: FWPM_PROVIDER_CONTEXT_CHANGE0 (fwpmtypes.h)
description: Change notification dispatched to subscribers. (FWPM_PROVIDER_CONTEXT_CHANGE0)
helpviewer_keywords: ["FWPM_PROVIDER_CONTEXT_CHANGE0","FWPM_PROVIDER_CONTEXT_CHANGE0 structure [Filtering]","fwp.fwpm_provider_context_change0_struct","fwpmtypes/FWPM_PROVIDER_CONTEXT_CHANGE0"]
old-location: fwp\fwpm_provider_context_change0_struct.htm
tech.root: fwp
ms.assetid: 78786d91-1e2f-4846-9636-8d5d6acf5a7d
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CONTEXT_CHANGE0, FWPM_PROVIDER_CONTEXT_CHANGE0 structure [Filtering], fwp.fwpm_provider_context_change0_struct, fwpmtypes/FWPM_PROVIDER_CONTEXT_CHANGE0
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
req.typenames: FWPM_PROVIDER_CONTEXT_CHANGE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_PROVIDER_CONTEXT_CHANGE0_
 - fwpmtypes/FWPM_PROVIDER_CONTEXT_CHANGE0_
 - FWPM_PROVIDER_CONTEXT_CHANGE0
 - fwpmtypes/FWPM_PROVIDER_CONTEXT_CHANGE0
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
 - FWPM_PROVIDER_CONTEXT_CHANGE0
---

# FWPM_PROVIDER_CONTEXT_CHANGE0 structure


## -description

The <b>FWPM_PROVIDER_CONTEXT_CHANGE0</b> structure contains a change notification dispatched to subscribers.

## -struct-fields

### -field changeType

Type of change.

See [FWPM_CHANGE_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_change_type) for more information.

### -field providerContextKey

GUID of the provider context that changed.

### -field providerContextId

LUID of the provider context that changed.

## -remarks

<b>FWPM_PROVIDER_CONTEXT_CHANGE0</b> is a specific implementation of FWPM_PROVIDER_CONTEXT_CHANGE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_CHANGE_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_change_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
