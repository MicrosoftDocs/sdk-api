---
UID: NS:processthreadsapi.OVERRIDE_PREFETCH_PARAMETER
title: OVERRIDE_PREFETCH_PARAMETER
description: 
helpviewer_keywords:
 - OVERRIDE_PREFETCH_PARAMETER
tech.root: processthreadsapi
ms.date: 01/29/2024
ms.keywords: '*LPOVERRIDE_PREFETCH_PARAMETER, *POVERRIDE_PREFETCH_PARAMETER, LPOVERRIDE_PREFETCH_PARAMETER, LPOVERRIDE_PREFETCH_PARAMETER structure pointer, OVERRIDE_PREFETCH_PARAMETER, OVERRIDE_PREFETCH_PARAMETER structure, _win32_override_prefetch_parameter_str, base.override_prefetch_parameter_str, processthreadsapi/LPOVERRIDE_PREFETCH_PARAMETER, processthreadsapi/OVERRIDE_PREFETCH_PARAMETER, winbase/LPOVERRIDE_PREFETCH_PARAMETER, winbase/OVERRIDE_PREFETCH_PARAMETER'
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.typenames: OVERRIDE_PREFETCH_PARAMETER
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - OVERRIDE_PREFETCH_PARAMETER
f1_keywords:
 - OVERRIDE_PREFETCH_PARAMETER
 - processthreadsapi/OVERRIDE_PREFETCH_PARAMETER
dev_langs:
 - c++
---

# OVERRIDE_PREFETCH_PARAMETER structure

## -description

Provides additional control over App Launch Prefetch (ALPF) functionality.

## -struct-fields

### -field Value

A unique identifier for differentiating an application view or mode.

## -remarks

App Launch Prefetch (ALPF) brings data and code pages into memory from disk before it's demanded. Prefetching monitors the data and code accessed during application startups and uses that information at the beginning of subsequent startups to read the code and data proactively in an efficient manner to improve performance.

If ALPF predicts incorrectly, the wrong pages may be fetched, slowing app launches. Applications with different "Views", such as Outlook Mail View or  Calendar View, may cause this issue by needing different pages of memory depending on the View. To solve this, applications can pass a prefetch parameter to their launch through the command line, which will provide a unique identifier to differentiate between Views or other scenarios that cause the ALPF standard prediction to fail.

In some cases, however, prefetching doesn't always resolve a failure successfully. For example, failures can happen when different code paths in the same executable require different pages but those startups were launched with the same prefetch parameter. To resolve these types of situations, the OVERRIDE_PREFETCH_PARAMETER can be used by an app to override the system prefetch parameter (see [SetProcessInformation function](nf-processthreadsapi-setprocessinformation.md)).

## Examples

The following code example shows how to use the prefetch override APIs when an app launches with a command-line prefetch parameter of 2.

1. Assume this is the first launch of an app, so the app instance designates itself as the primary process.
2. This primary process queries the maximum allowable value of an **OVERRIDE_PREFETCH_PARAMETER**.
3. Once confirmed that the override value is less than this maximum (when the app launches with a prefetch parameter of 2), it is overridden with a value of 9 by a call to the **[SetProcessInformation function](nf-processthreadsapi-setprocessinformation.md)** using a **ProcessInformation** value of **ProcessOverrideSubsequentPrefetchParameter**.
4. ALPF knows that an Override Prefetch Parameter has been set.
5. Another instance of GenericApp.exe is launched with a command-line prefetch parameter of 2. This instance will be transient as a primary process already exists.
6. Because an override from 2 to 9 has been set for this executable, ALPF will force this transient instance to launch in scenario 9 instead of 2.
7. ALPF now fetches appropriate pages for the primary process under scenario 2 and a separate set of pages for the other processes under scenario 9.
8. When the primary process of the app closes, the override will be removed, allowing the next launch of GenericApp.exe to become primary.

```cpp
int main (int argc, char *argv[]) {
    
    BOOL IsThisProcessPrimary;
    
    IsThisProcessPrimary = CheckIfProcessPrimary();
    
    if (!IsThisProcessPrimary) {    
    // This process is transient; it does not call the Override Prefetch Parameter API.
    PassTransientDataToPrimary(argc, argv);    
    goto Exit;    
    } else {    
    // This process is primary; attempt to call Override Prefetch Parameter    
    // before doing primary initialization.    
    SetOverridePrefetchParameter(9);
    
    InitializeThisProcessAsPrimary(argc, argv);    
    DisplayToUserAndWait();    
    }
    
Exit:
    
    return 0;    
}

DWORD SetOverridePrefetchParameter (UINT32 OverrideParameter) {
    
    OVERRIDE_PREFETCH_PARAMETER ParamInfo;    
    DWORD ErrorCode;    
    BOOL Win32Success;
    
    ZeroMemory(&ParamInfo, sizeof(ParamInfo));
    
    // Get the maximum Override Prefetch Parameter from    
    // GetProcessInformation.
    
    Win32Success = GetProcessInformation(GetCurrentProcess(),    
        ProcessOverrideSubsequentPrefetchParameter,    
        &ParamInfo,    
        sizeof(ParamInfo));
    
    if (!Win32Success) {    
        ErrorCode = GetLastError();
        goto Exit;    
    }
    
    if (OverrideParameter <= ParamInfo.OverrideScenarioId) {    
        ParamInfo.Value = OverrideParameter;    
    } else {    
        // The Override Prefetch Parameter requested isn't valid on this system.    
        // Continue to launch without setting an Override Prefetch Parameter.    
        ErrorCode = ERROR_INVALID_PARAMETER;    
        goto Exit;    
    }
    
    Win32Success = SetProcessInformation(GetCurrentProcess(),    
        ProcessOverrideSubsequentPrefetchParameter,    
        &ParamInfo,    
        sizeof(ParamInfo));
    
    if (!Win32Success) {    
        ErrorCode = GetLastError();    
        goto Exit;    
    }
    
    Exit:    
        ErrorCode = ERROR_SUCCESS;    
        return ErrorCode;    
}
```

## -see-also

[PROCESS_INFORMATION_CLASS enumeration](ne-processthreadsapi-process_information_class.md), [GetProcessInformation function](nf-processthreadsapi-getprocessinformation.md)