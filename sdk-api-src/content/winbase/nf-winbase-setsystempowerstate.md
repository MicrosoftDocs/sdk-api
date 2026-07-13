---
UID: NF:winbase.SetSystemPowerState
title: SetSystemPowerState function (winbase.h)
description: Suspends the system by shutting power down. Depending on the ForceFlag parameter, the function either suspends operation immediately or requests permission from all applications and device drivers before doing so.
helpviewer_keywords: ["SetSystemPowerState","SetSystemPowerState function","_win32_setsystempowerstate","base.setsystempowerstate","winbase/SetSystemPowerState"]
old-location: base\setsystempowerstate.htm
tech.root: base
ms.assetid: 58cf4e29-2a2e-499a-85ce-0034f4323cfe
ms.date: 12/05/2018
ms.keywords: SetSystemPowerState, SetSystemPowerState function, _win32_setsystempowerstate, base.setsystempowerstate, winbase/SetSystemPowerState
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetSystemPowerState
 - winbase/SetSystemPowerState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - api-ms-win-core-kernel32-legacy-l1-1-5.dll
 - api-ms-win-core-kernel32-legacy-l1-1-4.dll
 - api-ms-win-core-kernel32-legacy-l1-1-3.dll
 - api-ms-win-core-kernel32-legacy-l1-1-2.dll
 - api-ms-win-core-kernel32-legacy-l1-1-1.dll
 - api-ms-win-core-kernel32-legacy-l1-1-0.dll
 - Kernel32.dll
api_name:
 - SetSystemPowerState
---

# SetSystemPowerState function


## -description

<p class="CCE_Message">[<b>SetSystemPowerState</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Applications written for Windows Vista and later should use <a href="/windows/desktop/api/powrprof/nf-powrprof-setsuspendstate">SetSuspendState</a> instead.]

Suspends the system by shutting power down. Depending on the <i>ForceFlag</i> 
    parameter, the function either suspends operation immediately or requests permission from all applications and 
    device drivers before doing so.

## -parameters

### -param fSuspend [in]

If this parameter is <b>TRUE</b>, the system is suspended. If the parameter is 
      <b>FALSE</b>, the system hibernates.

### -param fForce [in]

This parameter has no effect.

## -returns

If power has been suspended and subsequently restored, the return value is nonzero.

If the system was not suspended, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege. To enable the 
    <b>SE_SHUTDOWN_NAME</b> privilege, use the 
    <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function. For more 
    information, see <a href="/windows/desktop/SecBP/changing-privileges-in-a-token">Changing Privileges in a 
    Token</a>.

If any application or driver denies permission to suspend operation, the function broadcasts a 
    <a href="/windows/desktop/Power/pbt-apmquerysuspendfailed">PBT_APMQUERYSUSPENDFAILED</a> event to each 
    application and driver. If power is suspended, this function returns only after system operation is resumed and 
    related <a href="/windows/desktop/Power/wm-powerbroadcast">WM_POWERBROADCAST</a> messages have been broadcast 
    to all applications and drivers.

This function is similar to the <a href="/windows/desktop/api/powrprof/nf-powrprof-setsuspendstate">SetSuspendState</a> 
    function.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0400 or later. For more 
    information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows 
    Headers</a>.

## -see-also

<a href="/windows/desktop/Power/pbt-apmquerysuspend">PBT_APMQUERYSUSPEND</a>



<a href="/windows/desktop/Power/pbt-apmquerysuspendfailed">PBT_APMQUERYSUSPENDFAILED</a>



<a href="/windows/desktop/Power/pbt-apmsuspend">PBT_APMSUSPEND</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-setsuspendstate">SetSuspendState</a>



<a href="/windows/desktop/Power/wm-powerbroadcast">WM_POWERBROADCAST</a>