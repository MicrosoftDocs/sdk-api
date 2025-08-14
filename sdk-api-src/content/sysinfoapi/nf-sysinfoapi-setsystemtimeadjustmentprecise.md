---
UID: NF:sysinfoapi.SetSystemTimeAdjustmentPrecise
title: SetSystemTimeAdjustmentPrecise function (sysinfoapi.h)
description: Enables or disables periodic time adjustments to the system's time-of-day clock. When enabled, such time adjustments can be used to synchronize the time of day with some other source of time information. (SetSystemTimeAdjustmentPrecise)
helpviewer_keywords: ["SetSystemTimeAdjustmentPrecise","SetSystemTimeAdjustmentPrecise function","base.setsystemtimeadjustmentprecise","sysinfoapi/SetSystemTimeAdjustmentPrecise"]
old-location: base\setsystemtimeadjustmentprecise.htm
tech.root: winprog
ms.assetid: 8B429BFC-9781-4434-9A2F-9E50E2BF299A
ms.date: 12/05/2018
ms.keywords: SetSystemTimeAdjustmentPrecise, SetSystemTimeAdjustmentPrecise function, base.setsystemtimeadjustmentprecise, sysinfoapi/SetSystemTimeAdjustmentPrecise
req.header: sysinfoapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mincore.lib
req.dll: Api-ms-win-core-version-l1-2-3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetSystemTimeAdjustmentPrecise
 - sysinfoapi/SetSystemTimeAdjustmentPrecise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
 - Api-ms-win-core-version-l1-2-3.dll
api_name:
 - SetSystemTimeAdjustmentPrecise
---

# SetSystemTimeAdjustmentPrecise function


## -description

Enables or disables periodic time adjustments to the system's time-of-day clock. When enabled, such time adjustments can be used to synchronize the time of day with some other source of time information.

## -parameters

### -param dwTimeAdjustment [in]

Supplies the adjusted clock update frequency.

### -param bTimeAdjustmentDisabled [in]

Supplies a flag which specifies the time adjustment mode that the system is to use.

A value of <b>TRUE</b> indicates that the system should synchronize time-of-day using its own internal mechanisms. In this case, the value of <i>dwTimeAdjustment</i> is ignored.

A value of <b>FALSE</b> indicates that the application is in control, and that the specified value of <i>dwTimeAdjustment</i> is to be added to the time-of-day clock at each clock update interrupt.

## -returns

If the function succeeds, the return value is non-zero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. One way the function can fail is if the caller does not possess the SE_SYSTEMTIME_NAME privilege.

## -remarks

To use this function, the caller must have system-time privilege (SE_SYSTEMTIME_NAME). This privilege is disabled by default. Use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function to enable the privilege before calling 
this function, then disable the privilege after the function call. For more information, see 
the code example below.


#### Examples

This sample demonstrates how to enable system-time privileges, adjust the system clock using <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustmentprecise">GetSystemTimeAdjustmentPrecise</a> and <b>SetSystemTimeAdjustmentPrecise</b>, and how to neatly print the current system-time adjustments.


```cpp

/****************************************************************** 
* 
* ObtainRequiredPrivileges 
* 
* Enables system time adjustment privilege. 
* 
******************************************************************/ 
HRESULT 
ObtainRequiredPrivileges() 
{ 
    HRESULT hr; 
    HANDLE hProcToken = NULL; 
    TOKEN_PRIVILEGES tp = {0}; 
    LUID luid; 

    if (!LookupPrivilegeValue(NULL, SE_SYSTEMTIME_NAME, &luid)) 
    { 
        hr = HRESULT_FROM_WIN32(GetLastError()); 
        printf("Failed to lookup privilege value. hr=0x%08x\n", hr); 
        return hr; 
    } 

    // get the token for our process 
    if (!OpenProcessToken(GetCurrentProcess(), 
    TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, 
    &hProcToken)) 
    { 
        hr = HRESULT_FROM_WIN32(GetLastError()); 
        printf("Failed to open process token. hr=0x%08x\n", hr); 
        return hr; 
    } 

    // Enable just the SYSTEMTIME privilege 
    tp.PrivilegeCount = 1; 
    tp.Privileges[0].Luid = luid; 
    tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED; 

    if (!AdjustTokenPrivileges(hProcToken, FALSE, &tp, 0, NULL, NULL)) 
    { 
        hr = HRESULT_FROM_WIN32(GetLastError()); 
        printf("Failed to adjust process token privileges. hr=0x%08x\n", hr); 
    } 
    else 
    { 
        hr = S_OK; 
        printf("Added SYSTEMTIME privilege to the process token\n"); 
    } 
    
    if (NULL != hProcToken) 
    { 
        CloseHandle(hProcToken); 
    } 
    return hr; 
} 

/****************************************************************** 
* 
* PrintCurrentClockAdjustments 
* 
* Prints current values of the system time adjustments. 
* 
******************************************************************/ 
void 
PrintCurrentClockAdjustments() 
{ 
    // More granular clock adjustments 
    DWORD64 ullCurrentAdjustment = 0; 
    DWORD64 ullTimeIncrement = 0; 
    BOOL bEnabledPrecise = 0; 
    HRESULT hrPrecise = S_OK; 

    // Legacy clock adjustments 
    DWORD dwCurrentAdjustment = 0; 
    DWORD dwTimeIncrement = 0; 
    BOOL bEnabled = 0; 
    HRESULT hr = S_OK; 

    if (!GetSystemTimeAdjustmentPrecise(&ullCurrentAdjustment, &ullTimeIncrement, &bEnabledPrecise)) 
    { 
        hrPrecise = HRESULT_FROM_WIN32(GetLastError()); 
    } 

    if (!GetSystemTimeAdjustment(&dwCurrentAdjustment, &dwTimeIncrement, &bEnabled)) 
    { 
        hr = HRESULT_FROM_WIN32(GetLastError()); 
    } 

    printf("Precise_ADJ:%I64u Precise_INCR:%I64u Precise_EN:%d Precise_hr:0x%08x ADJ:%u INCR:%u EN:%d hr:0x%08x\n", 
            ullCurrentAdjustment, ullTimeIncrement, bEnabledPrecise, hrPrecise, 
            dwCurrentAdjustment, dwTimeIncrement, bEnabled, hr); 
} 

/****************************************************************** 
* 
* RunNewAdjustmentSequence 
* 
* Adjust the system time using high-resolution 
* GetSystemTimeAdjustmentPrecise() and SetSystemTimeAdjustmentPrecise() API. 
* 
******************************************************************/ 
void 
RunNewAdjustmentSequence(DWORD dwPPMAdjustment) 
{ 
    DWORD64 ullCurrentAdjustment = 0; 
    DWORD64 ullTimeIncrement = 0; 
    BOOL bEnabledPrecise = 0; 
    LARGE_INTEGER liPerfCounterFrequency = {0}; 
    DWORD dwNewAdjustmentUnits; 
    const DWORD cMicroSecondsPerSecond = 1000000; 

    if (dwPPMAdjustment > 1000) 
    { 
        printf("Adjustment too large. Skipping new adjustment sequence.\n"); 
        return; 
    } 

    printf("Starting adjustment sequence using new API...\n"); 

    if (!GetSystemTimeAdjustmentPrecise(&ullCurrentAdjustment, &ullTimeIncrement, &bEnabledPrecise)) 
    { 
        printf("Failed to read the system time adjustment. Adjustment sequence aborted. hr:0x%08x\n", 
        HRESULT_FROM_WIN32(GetLastError())); 
        return; 
    } 

    (void)QueryPerformanceFrequency(&liPerfCounterFrequency); 
    printf("System Performance Counter Frequency: %I64u\n", 
    liPerfCounterFrequency.QuadPart); 


    dwNewAdjustmentUnits = (DWORD)(((float) dwPPMAdjustment * liPerfCounterFrequency.QuadPart/ cMicroSecondsPerSecond)); 

    printf("Adjusting the system clock by +%d PPM (+%d new units)\n", 
    dwPPMAdjustment, dwNewAdjustmentUnits); 

    if (!SetSystemTimeAdjustmentPrecise(ullCurrentAdjustment + dwNewAdjustmentUnits, FALSE)) 
    { 
        printf("Failed to set the system time adjustment. hr:0x%08x\n", 
        HRESULT_FROM_WIN32(GetLastError())); 
    } 

    PrintCurrentClockAdjustments(); 

    printf("Restoring system clock adjustment settings\n"); 

    if (!SetSystemTimeAdjustmentPrecise(ullCurrentAdjustment, FALSE)) 
    { 
        printf("Failed to set the system time adjustment. hr:0x%08x\n", 
        HRESULT_FROM_WIN32(GetLastError())); 
    } 

    PrintCurrentClockAdjustments(); 

    printf("Adjusting the system clock by -%d PPM (-%d new units)\n", 
    dwPPMAdjustment, dwNewAdjustmentUnits); 

    if (!SetSystemTimeAdjustmentPrecise(ullCurrentAdjustment - dwNewAdjustmentUnits, FALSE)) 
    { 
        printf("Failed to set the system time adjustment. hr:0x%08x\n", 
        HRESULT_FROM_WIN32(GetLastError())); 
    } 

    PrintCurrentClockAdjustments(); 

    printf("Restoring system clock adjustment settings\n"); 

    if (!SetSystemTimeAdjustmentPrecise(ullCurrentAdjustment, FALSE)) 
    { 
        printf("Failed to set the system time adjustment. hr:0x%08x\n", 
        HRESULT_FROM_WIN32(GetLastError())); 
    } 

    PrintCurrentClockAdjustments(); 

    printf("Adjustment sequence complete\n\n"); 
}
```

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustmentprecise">GetSystemTimeAdjustmentPrecise</a>
