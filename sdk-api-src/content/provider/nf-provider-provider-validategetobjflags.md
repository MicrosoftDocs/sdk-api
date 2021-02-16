---
UID: NF:provider.Provider.ValidateGetObjFlags
title: Provider::ValidateGetObjFlags (provider.h)
description: The ValidateGetObjFlags method determines whether a set of flags is valid for an instance retrieval operation.
helpviewer_keywords: ["?ValidateGetObjFlags@Provider@@MAEJJ@Z","?ValidateGetObjFlags@Provider@@MEAAJJ@Z","Provider interface [Windows Management Instrumentation]","ValidateGetObjFlags method","Provider.ValidateGetObjFlags","Provider::ValidateGetObjFlags","ValidateGetObjFlags","ValidateGetObjFlags method [Windows Management Instrumentation]","ValidateGetObjFlags method [Windows Management Instrumentation]","Provider interface","_hmm_provider_validategetobjflags","provider/Provider::ValidateGetObjFlags","wmi.provider_validategetobjflags"]
old-location: wmi\provider_validategetobjflags.htm
tech.root: wmi
ms.assetid: 5090c47b-062b-4359-b03b-0d05c225447d
ms.date: 12/05/2018
ms.keywords: ?ValidateGetObjFlags@Provider@@MAEJJ@Z, ?ValidateGetObjFlags@Provider@@MEAAJJ@Z, Provider interface [Windows Management Instrumentation],ValidateGetObjFlags method, Provider.ValidateGetObjFlags, Provider::ValidateGetObjFlags, ValidateGetObjFlags, ValidateGetObjFlags method [Windows Management Instrumentation], ValidateGetObjFlags method [Windows Management Instrumentation],Provider interface, _hmm_provider_validategetobjflags, provider/Provider::ValidateGetObjFlags, wmi.provider_validategetobjflags
req.header: provider.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Provider::ValidateGetObjFlags
 - provider/Provider::ValidateGetObjFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.ValidateGetObjFlags
 - ?ValidateGetObjFlags@Provider@@MAEJJ@Z
 - ?ValidateGetObjFlags@Provider@@MEAAJJ@Z
---

# Provider::ValidateGetObjFlags


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>ValidateGetObjFlags</b> method determines whether a set of flags is valid for an instance retrieval operation.

## -parameters

### -param lFlags

Bitmask of flags that are validated.

## -returns

Returns <b>WBEM_S_NO_ERROR</b> if the flags are valid and <b>WBEM_E_UNSUPPORTED_PARAMETER</b> if one or more flags are not valid.

## -remarks

At present, the <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class does not support any retrieval flags. Therefore, if <i>lFlags</i> is set to a value other than zero (0),  <b>Provider::ValidateGetObjFlags</b> automatically returns <b>WBEM_E_UNSUPPORTED_PARAMETER</b>.

Framework providers must override this method to validate flags that are unknown to the base <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class.