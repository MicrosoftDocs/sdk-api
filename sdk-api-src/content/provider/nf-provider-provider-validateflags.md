---
UID: NF:provider.Provider.ValidateFlags
title: Provider::ValidateFlags (provider.h)
description: The ValidateFlags method determines whether a set of flags is valid.
helpviewer_keywords: ["Provider interface [Windows Management Instrumentation]","ValidateFlags method","Provider.ValidateFlags","Provider::ValidateFlags","ValidateFlags","ValidateFlags method [Windows Management Instrumentation]","ValidateFlags method [Windows Management Instrumentation]","Provider interface","_hmm_provider_validateflags","provider/Provider::ValidateFlags","wmi.provider_validateflags"]
old-location: wmi\provider_validateflags.htm
tech.root: wmi
ms.assetid: 1d6d1006-99b9-4646-a5c4-835940ce3ac0
ms.date: 12/05/2018
ms.keywords: Provider interface [Windows Management Instrumentation],ValidateFlags method, Provider.ValidateFlags, Provider::ValidateFlags, ValidateFlags, ValidateFlags method [Windows Management Instrumentation], ValidateFlags method [Windows Management Instrumentation],Provider interface, _hmm_provider_validateflags, provider/Provider::ValidateFlags, wmi.provider_validateflags
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
 - Provider::ValidateFlags
 - provider/Provider::ValidateFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - Provider.ValidateFlags
---

# Provider::ValidateFlags


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/provider/nl-provider-provider">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>ValidateFlags</b> method determines whether a set of flags is valid.

## -parameters

### -param lFlags

Bitmask of flags that are validated.

### -param lAcceptableFlags

Bitmask of <i>IFlags</i> values that are acceptable to the calling method. For more information, see Remarks.

## -returns

Returns <b>WBEM_S_NO_ERROR</b> if the flags are valid and <b>WBEM_E_UNSUPPORTED_PARAMETER</b> if one or more flags are not valid.

## -remarks

This helper method can be called by an override of any of the following virtual methods to indicate which flags are acceptable as arguments to the virtual method:

<ul>
<li>
<a href="/windows/desktop/api/provider/nf-provider-provider-validatedeletionflags">Provider::ValidateDeletionFlags</a>
</li>
<li>
<a href="/windows/desktop/api/provider/nf-provider-provider-validateenumerationflags">Provider::ValidateEnumerationFlags</a>
</li>
<li>
<a href="/windows/desktop/api/provider/nf-provider-provider-validategetobjflags">Provider::ValidateGetObjFlags</a>
</li>
<li>
<a href="/windows/desktop/api/provider/nf-provider-provider-validatemethodflags">Provider::ValidateMethodFlags</a>
</li>
<li>
<a href="/windows/desktop/api/provider/nf-provider-provider-validateputinstanceflags">Provider::ValidatePutInstanceFlags</a>
</li>
<li>
<a href="/windows/desktop/api/provider/nf-provider-provider-validatequeryflags">Provider::ValidateQueryFlags</a>
</li>
</ul>
The values for <i>IAcceptableFlags</i> are limited to the <a href="/previous-versions/windows/desktop/legacy/mt432263(v=vs.85)">FlagDefs</a> enumeration defined as the following:


```cpp
    enum FlagDefs
    {
        EnumerationFlags = 0,
        GetObjFlags = 0,
        MethodFlags = 0,
        DeletionFlags = 0,
        PutInstanceFlags = (WBEM_FLAG_CREATE_OR_UPDATE |
                            WBEM_FLAG_CREATE_ONLY |
                            WBEM_FLAG_UPDATE_ONLY),
        QueryFlags = 0
    };
```