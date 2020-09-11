---
UID: NF:sysinfoapi.GetSystemTime
title: GetSystemTime function (sysinfoapi.h)
description: Retrieves the current system date and time. The system time is expressed in Coordinated Universal Time (UTC).
helpviewer_keywords: ["GetSystemTime","GetSystemTime function","_win32_getsystemtime","base.getsystemtime","sysinfoapi/GetSystemTime"]
old-location: base\getsystemtime.htm
tech.root: winprog
ms.assetid: 9ed8386b-f035-446f-b0f8-12e0d3f23aac
ms.date: 12/05/2018
ms.keywords: GetSystemTime, GetSystemTime function, _win32_getsystemtime, base.getsystemtime, sysinfoapi/GetSystemTime
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - GetSystemTime
 - sysinfoapi/GetSystemTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
 - GetSystemTime
---

# GetSystemTime function


## -description

Retrieves the current system date and time. The system time is expressed in Coordinated Universal Time (UTC).

To retrieve the current system date and time in local time, use the <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlocaltime">GetLocalTime</a> function.

## -parameters

### -param lpSystemTime [out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure to receive the current system date and time. The <i>lpSystemTime</i> parameter must not be <b>NULL</b>. Using <b>NULL</b> will result in an access violation.

## -remarks

To set the current system date and time, use the <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setsystemtime">SetSystemTime</a> function.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>.

<div class="code"></div>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getlocaltime">GetLocalTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment">GetSystemTimeAdjustment</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime">GetSystemTimeAsFileTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setsystemtime">SetSystemTime</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-time">System Time</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/time-functions">Time Functions</a>

