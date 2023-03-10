---
UID: NF:provider.Provider.ValidateMethodFlags
title: Provider::ValidateMethodFlags (provider.h)
description: The ValidateMethodFlags method determines whether a set of flags is valid for an execute method operation.
helpviewer_keywords: ["?ValidateMethodFlags@Provider@@MAEJJ@Z","?ValidateMethodFlags@Provider@@MEAAJJ@Z","Provider interface [Windows Management Instrumentation]","ValidateMethodFlags method","Provider.ValidateMethodFlags","Provider::ValidateMethodFlags","ValidateMethodFlags","ValidateMethodFlags method [Windows Management Instrumentation]","ValidateMethodFlags method [Windows Management Instrumentation]","Provider interface","_hmm_provider_validatemethodflags","provider/Provider::ValidateMethodFlags","wmi.provider_validatemethodflags"]
old-location: wmi\provider_validatemethodflags.htm
tech.root: wmi
ms.assetid: febc48d8-8952-4e2f-80fc-40344908f8b2
ms.date: 12/05/2018
ms.keywords: ?ValidateMethodFlags@Provider@@MAEJJ@Z, ?ValidateMethodFlags@Provider@@MEAAJJ@Z, Provider interface [Windows Management Instrumentation],ValidateMethodFlags method, Provider.ValidateMethodFlags, Provider::ValidateMethodFlags, ValidateMethodFlags, ValidateMethodFlags method [Windows Management Instrumentation], ValidateMethodFlags method [Windows Management Instrumentation],Provider interface, _hmm_provider_validatemethodflags, provider/Provider::ValidateMethodFlags, wmi.provider_validatemethodflags
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
 - Provider::ValidateMethodFlags
 - provider/Provider::ValidateMethodFlags
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
 - Provider.ValidateMethodFlags
 - ?ValidateMethodFlags@Provider@@MAEJJ@Z
 - ?ValidateMethodFlags@Provider@@MEAAJJ@Z
---

# Provider::ValidateMethodFlags


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>ValidateMethodFlags</b> method determines whether a set of flags is valid for an execute method operation.

## -parameters

### -param lFlags

Bitmask of flags that are validated.

## -returns

Returns <b>WBEM_S_NO_ERROR</b> if the flags are valid and <b>WBEM_E_UNSUPPORTED_PARAMETER</b> if one or more flags are not valid.

## -remarks

At present, the <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class does not support any method flags. Therefore, if <i>lFlags</i> is set to a value other than zero (0),  <b>Provider::ValidateMethodFlags</b> automatically returns <b>WBEM_E_UNSUPPORTED_PARAMETER</b>.

Framework providers must override this method to validate flags that are unknown to the base <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class.