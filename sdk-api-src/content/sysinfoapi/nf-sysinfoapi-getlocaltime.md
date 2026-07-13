---
UID: NF:sysinfoapi.GetLocalTime
title: GetLocalTime function (sysinfoapi.h)
description: Retrieves the current local date and time.
helpviewer_keywords: ["GetLocalTime","GetLocalTime function","_win32_getlocaltime","base.getlocaltime","sysinfoapi/GetLocalTime"]
old-location: base\getlocaltime.htm
tech.root: winprog
ms.assetid: a63fcd36-de48-4437-a823-837884cc2bf9
ms.date: 12/05/2018
ms.keywords: GetLocalTime, GetLocalTime function, _win32_getlocaltime, base.getlocaltime, sysinfoapi/GetLocalTime
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
 - GetLocalTime
 - sysinfoapi/GetLocalTime
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
 - GetLocalTime
---

# GetLocalTime function


## -description

Retrieves the current local date and time.

To retrieve the current date and time in Coordinated Universal Time (UTC) format, use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a> function.

## -parameters

### -param lpSystemTime [out]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure to receive the current local date and time.

## -remarks

To set the current local date and time, use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setlocaltime">SetLocalTime</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a>



<a href="/windows/desktop/SysInfo/local-time">Local Time</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setlocaltime">SetLocalTime</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>