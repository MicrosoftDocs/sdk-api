---
UID: NF:provider.Provider.ValidatePutInstanceFlags
title: Provider::ValidatePutInstanceFlags (provider.h)
description: The ValidatePutInstanceFlags method determines whether a set of flags is valid for an instance update operation.
helpviewer_keywords: ["?ValidatePutInstanceFlags@Provider@@MAEJJ@Z","?ValidatePutInstanceFlags@Provider@@MEAAJJ@Z","Provider interface [Windows Management Instrumentation]","ValidatePutInstanceFlags method","Provider.ValidatePutInstanceFlags","Provider::ValidatePutInstanceFlags","ValidatePutInstanceFlags","ValidatePutInstanceFlags method [Windows Management Instrumentation]","ValidatePutInstanceFlags method [Windows Management Instrumentation]","Provider interface","_hmm_provider_validateputinstanceflags","provider/Provider::ValidatePutInstanceFlags","wmi.provider_validateputinstanceflags"]
old-location: wmi\provider_validateputinstanceflags.htm
tech.root: wmi
ms.assetid: dd7a480e-9569-45ed-a46d-218c1a9cf2db
ms.date: 12/05/2018
ms.keywords: ?ValidatePutInstanceFlags@Provider@@MAEJJ@Z, ?ValidatePutInstanceFlags@Provider@@MEAAJJ@Z, Provider interface [Windows Management Instrumentation],ValidatePutInstanceFlags method, Provider.ValidatePutInstanceFlags, Provider::ValidatePutInstanceFlags, ValidatePutInstanceFlags, ValidatePutInstanceFlags method [Windows Management Instrumentation], ValidatePutInstanceFlags method [Windows Management Instrumentation],Provider interface, _hmm_provider_validateputinstanceflags, provider/Provider::ValidatePutInstanceFlags, wmi.provider_validateputinstanceflags
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
 - Provider::ValidatePutInstanceFlags
 - provider/Provider::ValidatePutInstanceFlags
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
 - Provider.ValidatePutInstanceFlags
 - ?ValidatePutInstanceFlags@Provider@@MAEJJ@Z
 - ?ValidatePutInstanceFlags@Provider@@MEAAJJ@Z
---

# Provider::ValidatePutInstanceFlags


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>ValidatePutInstanceFlags</b> method determines whether a set of flags is valid for an instance update operation.

## -parameters

### -param lFlags

Bitmask of flags that are validated.

## -returns

Returns <b>WBEM_S_NO_ERROR</b> if the flags are valid and <b>WBEM_E_UNSUPPORTED_PARAMETER</b> if one or more flags are not valid.

## -remarks

Framework providers can override this method to validate flags that are unknown to the base <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class.

At present, the <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class supports the following update flags:

<ul>
<li><b>WBEM_FLAG_CREATE_ONLY</b></li>
<li><b>WBEM_FLAG_CREATE_OR_UPDATE</b></li>
<li><b>WBEM_FLAG_UPDATE_ONLY</b></li>
</ul>