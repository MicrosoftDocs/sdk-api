---
UID: NS:fwpmtypes.FWPM_CALLOUT_ENUM_TEMPLATE0_
title: FWPM_CALLOUT_ENUM_TEMPLATE0 (fwpmtypes.h)
description: Used for limiting callout enumerations.
helpviewer_keywords: ["FWPM_CALLOUT_ENUM_TEMPLATE0","FWPM_CALLOUT_ENUM_TEMPLATE0 structure [Filtering]","fwp.fwpm_callout_enum_template0_struct","fwpmtypes/FWPM_CALLOUT_ENUM_TEMPLATE0"]
old-location: fwp\fwpm_callout_enum_template0_struct.htm
tech.root: fwp
ms.assetid: 10997be6-069d-4d1a-a6b1-1a1e0a5359c5
ms.date: 12/05/2018
ms.keywords: FWPM_CALLOUT_ENUM_TEMPLATE0, FWPM_CALLOUT_ENUM_TEMPLATE0 structure [Filtering], fwp.fwpm_callout_enum_template0_struct, fwpmtypes/FWPM_CALLOUT_ENUM_TEMPLATE0
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
req.typenames: FWPM_CALLOUT_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_CALLOUT_ENUM_TEMPLATE0_
 - fwpmtypes/FWPM_CALLOUT_ENUM_TEMPLATE0_
 - FWPM_CALLOUT_ENUM_TEMPLATE0
 - fwpmtypes/FWPM_CALLOUT_ENUM_TEMPLATE0
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
 - FWPM_CALLOUT_ENUM_TEMPLATE0
---

# FWPM_CALLOUT_ENUM_TEMPLATE0 structure


## -description

The <b>FWPM_CALLOUT_ENUM_TEMPLATE0</b> structure is used for limiting callout enumerations.

## -struct-fields

### -field providerKey

Uniquely identifies the provider associated with the callout. If this member is non-NULL, only objects associated with the specified provider will be returned.

### -field layerKey

Uniquely identifies a layer. If this member is non-NULL, only callouts associated with the specified layer will be returned.

## -remarks

<b>FWPM_CALLOUT_ENUM_TEMPLATE0</b> is a specific implementation of FWPM_CALLOUT_ENUM_TEMPLATE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>