---
UID: NF:sysinfoapi.SetLocalTime
title: SetLocalTime function (sysinfoapi.h)
description: Sets the current local time and date.
helpviewer_keywords: ["SetLocalTime","SetLocalTime function","_win32_setlocaltime","base.setlocaltime","sysinfoapi/SetLocalTime"]
old-location: base\setlocaltime.htm
tech.root: winprog
ms.assetid: c2d2bac7-4171-4b8b-81e8-0e8a1b2794e6
ms.date: 12/05/2018
ms.keywords: SetLocalTime, SetLocalTime function, _win32_setlocaltime, base.setlocaltime, sysinfoapi/SetLocalTime
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
 - SetLocalTime
 - sysinfoapi/SetLocalTime
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
 - API-MS-Win-Core-SysInfo-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - SetLocalTime
---

# SetLocalTime function


## -description

Sets the current local time and date.

## -parameters

### -param lpSystemTime [in]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the new local date and time. 




The <b>wDayOfWeek</b> member of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure is ignored.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The calling process must have the SE_SYSTEMTIME_NAME privilege. This privilege is disabled by default. The 
<b>SetLocalTime</b> function enables the SE_SYSTEMTIME_NAME privilege before changing the local time and disables the privilege before returning. For more information, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a>.

The system uses UTC internally. Therefore, when you call 
<b>SetLocalTime</b>, the system uses the current time zone information to perform the conversion, including the daylight saving time setting. Note that the system uses the daylight saving time setting of the current time, not the new time you are setting. Therefore, to ensure the correct result, call 
<b>SetLocalTime</b> a second time, now that the first call has updated the daylight saving time setting.

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlocaltime">GetLocalTime</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="/windows/desktop/SysInfo/local-time">Local Time</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment">SetSystemTimeAdjustment</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>