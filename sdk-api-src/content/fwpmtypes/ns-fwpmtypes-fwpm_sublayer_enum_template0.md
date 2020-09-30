---
UID: NS:fwpmtypes.FWPM_SUBLAYER_ENUM_TEMPLATE0_
title: FWPM_SUBLAYER_ENUM_TEMPLATE0 (fwpmtypes.h)
description: Is used for enumerating sublayers.
helpviewer_keywords: ["FWPM_SUBLAYER_ENUM_TEMPLATE0","FWPM_SUBLAYER_ENUM_TEMPLATE0 structure [Filtering]","fwp.fwpm_sublayer_enum_template0_struct","fwpmtypes/FWPM_SUBLAYER_ENUM_TEMPLATE0"]
old-location: fwp\fwpm_sublayer_enum_template0_struct.htm
tech.root: fwp
ms.assetid: 4f05730c-7bf6-4bf4-b3ec-d8fe138b2228
ms.date: 12/05/2018
ms.keywords: FWPM_SUBLAYER_ENUM_TEMPLATE0, FWPM_SUBLAYER_ENUM_TEMPLATE0 structure [Filtering], fwp.fwpm_sublayer_enum_template0_struct, fwpmtypes/FWPM_SUBLAYER_ENUM_TEMPLATE0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_SUBLAYER_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_SUBLAYER_ENUM_TEMPLATE0_
 - fwpmtypes/FWPM_SUBLAYER_ENUM_TEMPLATE0_
 - FWPM_SUBLAYER_ENUM_TEMPLATE0
 - fwpmtypes/FWPM_SUBLAYER_ENUM_TEMPLATE0
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
 - FWPM_SUBLAYER_ENUM_TEMPLATE0
---

# FWPM_SUBLAYER_ENUM_TEMPLATE0 structure


## -description

The <b>FWPM_SUBLAYER_ENUM_TEMPLATE0</b> structure is used for enumerating sublayers.

## -struct-fields

### -field providerKey

Uniquely identifies the provider associated with this sublayer. If this value is non-NULL, only options with the specifies provider will be returned.

## -remarks

<b>FWPM_SUBLAYER_ENUM_TEMPLATE0</b> is a specific implementation of FWPM_SUBLAYER_ENUM_TEMPLATE. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>