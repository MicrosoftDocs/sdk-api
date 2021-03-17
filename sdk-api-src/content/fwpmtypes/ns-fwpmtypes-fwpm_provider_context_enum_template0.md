---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0_
title: FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0 (fwpmtypes.h)
description: Used for enumerating provider contexts.
helpviewer_keywords: ["FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0","FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0 structure [Filtering]","fwp.fwpm_provider_context_enum_template0_struct","fwpmtypes/FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0"]
old-location: fwp\fwpm_provider_context_enum_template0_struct.htm
tech.root: fwp
ms.assetid: 0d43931a-93ae-43dd-9c5b-3989799e7b60
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0, FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0 structure [Filtering], fwp.fwpm_provider_context_enum_template0_struct, fwpmtypes/FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0
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
req.typenames: FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0_
 - fwpmtypes/FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0_
 - FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0
 - fwpmtypes/FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0
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
 - FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0
---

# FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0 structure


## -description

The <b>FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</b> structure is used for enumerating provider contexts.

## -struct-fields

### -field providerKey

Uniquely identifies a provider. If this value is non-NULL, only options with the specifies provider will be returned.

### -field providerContextType

Only return provider contexts of the specified type.

See [FWPM_PROVIDER_CONTEXT_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type) for more information.

## -remarks

<b>FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</b> is a specific implementation of FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_PROVIDER_CONTEXT_TYPE](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>