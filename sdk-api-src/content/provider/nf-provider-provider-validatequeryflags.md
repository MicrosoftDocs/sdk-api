---
UID: NF:provider.Provider.ValidateQueryFlags
title: Provider::ValidateQueryFlags (provider.h)
description: The ValidateQueryFlags method determines whether a set of flags is valid for a query operation.
helpviewer_keywords: ["?ValidateQueryFlags@Provider@@MAEJJ@Z","?ValidateQueryFlags@Provider@@MEAAJJ@Z","Provider interface [Windows Management Instrumentation]","ValidateQueryFlags method","Provider.ValidateQueryFlags","Provider::ValidateQueryFlags","ValidateQueryFlags","ValidateQueryFlags method [Windows Management Instrumentation]","ValidateQueryFlags method [Windows Management Instrumentation]","Provider interface","_hmm_provider_validatequeryflags","provider/Provider::ValidateQueryFlags","wmi.provider_validatequeryflags"]
old-location: wmi\provider_validatequeryflags.htm
tech.root: wmi
ms.assetid: b35e6f2f-7d40-4b9b-833d-63efafd06a20
ms.date: 12/05/2018
ms.keywords: ?ValidateQueryFlags@Provider@@MAEJJ@Z, ?ValidateQueryFlags@Provider@@MEAAJJ@Z, Provider interface [Windows Management Instrumentation],ValidateQueryFlags method, Provider.ValidateQueryFlags, Provider::ValidateQueryFlags, ValidateQueryFlags, ValidateQueryFlags method [Windows Management Instrumentation], ValidateQueryFlags method [Windows Management Instrumentation],Provider interface, _hmm_provider_validatequeryflags, provider/Provider::ValidateQueryFlags, wmi.provider_validatequeryflags
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
 - Provider::ValidateQueryFlags
 - provider/Provider::ValidateQueryFlags
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
 - Provider.ValidateQueryFlags
 - ?ValidateQueryFlags@Provider@@MAEJJ@Z
 - ?ValidateQueryFlags@Provider@@MEAAJJ@Z
---

# Provider::ValidateQueryFlags


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>ValidateQueryFlags</b> method determines whether a set of flags is valid for a query operation.

## -parameters

### -param lFlags

Bitmask of flags that are validated.

## -returns

Returns <b>WBEM_S_NO_ERROR</b> if the flags are valid and <b>WBEM_E_UNSUPPORTED_PARAMETER</b> if one or more flags are not valid.

## -remarks

At present, the <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class does not support any query flags. Therefore, if <i>lFlags</i> is set to a value other than zero (0),  <b>Provider::ValidateQueryFlags</b> automatically returns <b>WBEM_E_UNSUPPORTED_PARAMETER</b>.

Framework providers must override this method to validate flags that are unknown to the base <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class.