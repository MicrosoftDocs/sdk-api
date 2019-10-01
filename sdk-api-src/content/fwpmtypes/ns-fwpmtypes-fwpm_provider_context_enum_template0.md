---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0_
title: FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0 (fwpmtypes.h)
author: windows-sdk-content
description: Used for enumerating provider contexts.
old-location: fwp\fwpm_provider_context_enum_template0_struct.htm
tech.root: fwp
ms.assetid: 0d43931a-93ae-43dd-9c5b-3989799e7b60
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0, FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0 structure [Filtering], fwp.fwpm_provider_context_enum_template0_struct, fwpmtypes/FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0
ms.topic: struct
f1_keywords: 
 - "fwpmtypes/FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0
targetos: Windows
req.typenames: FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
---

# FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0 structure


## -description


The <b>FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</b> structure is used for enumerating provider contexts.


## -struct-fields




### -field providerKey

Uniquely identifies a provider. If this value is non-NULL, only options with the specifies provider will be returned.


### -field providerContextType

Only return provider contexts of the specified type.

See <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type_">FWPM_PROVIDER_CONTEXT_TYPE</a> for more information.


## -remarks



<b>FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</b> is a specific implementation of FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type_">FWPM_PROVIDER_CONTEXT_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

