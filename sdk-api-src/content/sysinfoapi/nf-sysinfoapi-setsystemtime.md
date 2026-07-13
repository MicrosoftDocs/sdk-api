---
UID: NF:sysinfoapi.SetSystemTime
title: SetSystemTime function (sysinfoapi.h)
description: Sets the current system time and date. The system time is expressed in Coordinated Universal Time (UTC).
helpviewer_keywords: ["SetSystemTime","SetSystemTime function","_win32_setsystemtime","base.setsystemtime","sysinfoapi/SetSystemTime"]
old-location: base\setsystemtime.htm
tech.root: winprog
ms.assetid: 0768794d-de61-4d5c-96ad-4c4711c72584
ms.date: 12/05/2018
ms.keywords: SetSystemTime, SetSystemTime function, _win32_setsystemtime, base.setsystemtime, sysinfoapi/SetSystemTime
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - SetSystemTime
 - sysinfoapi/SetSystemTime
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
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - SetSystemTime
---

# SetSystemTime function


## -description

Sets the current system time and date. The system time is expressed in Coordinated Universal Time (UTC).

## -parameters

### -param lpSystemTime [in]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the new system date and time. 




The <b>wDayOfWeek</b> member of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure is ignored.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The calling process must have the SE_SYSTEMTIME_NAME privilege. This privilege is disabled by default. The 
<b>SetSystemTime</b> function enables the SE_SYSTEMTIME_NAME privilege before changing the system time and disables the privilege before returning. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment">SetSystemTimeAdjustment</a>



<a href="/windows/desktop/SysInfo/system-time">System Time</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>