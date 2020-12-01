---
UID: NF:powrprof.SetSuspendState
title: SetSuspendState function (powrprof.h)
description: Suspends the system by shutting power down. Depending on the Hibernate parameter, the system either enters a suspend (sleep) state or hibernation (S4).
helpviewer_keywords: ["SetSuspendState","SetSuspendState function","_win32_setsuspendstate","base.setsuspendstate","powrprof/SetSuspendState"]
old-location: base\setsuspendstate.htm
tech.root: base
ms.assetid: 63cb6574-8c0d-4bcb-832c-7088447a5c04
ms.date: 12/05/2018
ms.keywords: SetSuspendState, SetSuspendState function, _win32_setsuspendstate, base.setsuspendstate, powrprof/SetSuspendState
req.header: powrprof.h
req.include-header: 
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
req.lib: PowrProf.lib
req.dll: PowrProf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetSuspendState
 - powrprof/SetSuspendState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - PowrProf.dll
api_name:
 - SetSuspendState
---

# SetSuspendState function


## -description

Suspends the system by shutting power down. Depending on the <i>Hibernate</i> 
    parameter, the system either enters a suspend (sleep) state or hibernation (S4).

## -parameters

### -param bHibernate [in]

If this parameter is <b>TRUE</b>, the system hibernates. If the parameter is 
      <b>FALSE</b>, the system is suspended.

### -param bForce [in]

This parameter has no effect.

### -param bWakeupEventsDisabled [in]

If this parameter is <b>TRUE</b>, the system disables all wake events. If the parameter 
      is <b>FALSE</b>, any system wake events remain enabled.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The calling process must have the <b>SE_SHUTDOWN_NAME</b> privilege. To enable the 
    <b>SE_SHUTDOWN_NAME</b> privilege, use the 
    <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a> function. For more 
    information, see <a href="/windows/desktop/SecBP/changing-privileges-in-a-token">Changing Privileges in a 
    Token</a>.

An application may use <b>SetSuspendState</b> to 
    transition the system from the working state to the standby (sleep), or optionally, hibernate (S4) state. This 
    function is similar to the <a href="/windows/desktop/api/winbase/nf-winbase-setsystempowerstate">SetSystemPowerState</a> 
    function.

For more information on using PowrProf.h, see 
    <a href="/windows/desktop/Power/power-schemes">Power Schemes</a>. For information about events that can wake the system, see <a href="/windows/desktop/Power/system-wake-up-events">System Wake-up Events</a>.

## -see-also

<a href="/windows/desktop/Power/pbt-apmquerysuspend">PBT_APMQUERYSUSPEND</a>



<a href="/windows/desktop/Power/pbt-apmsuspend">PBT_APMSUSPEND</a>



<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>