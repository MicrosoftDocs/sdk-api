---
UID: NF:sysinfoapi.GetSystemTimePreciseAsFileTime
title: GetSystemTimePreciseAsFileTime function (sysinfoapi.h)
description: GetSystemTimePreciseAsFileTime function retrieves the current system date and time with the highest possible level of precision (&lt;1us). The retrieved information is in Coordinated Universal Time (UTC) format.
helpviewer_keywords: ["GetSystemTimePreciseAsFileTime","GetSystemTimePreciseAsFileTime function","base.getsystemtimepreciseasfiletime","sysinfoapi/GetSystemTimePreciseAsFileTime"]
old-location: base\getsystemtimepreciseasfiletime.htm
tech.root: winprog
ms.assetid: 8949C2D4-AE5A-4E18-9B06-F2F13EFA8A5E
ms.date: 12/05/2018
ms.keywords: GetSystemTimePreciseAsFileTime, GetSystemTimePreciseAsFileTime function, base.getsystemtimepreciseasfiletime, sysinfoapi/GetSystemTimePreciseAsFileTime
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - GetSystemTimePreciseAsFileTime
 - sysinfoapi/GetSystemTimePreciseAsFileTime
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
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetSystemTimePreciseAsFileTime
---

# GetSystemTimePreciseAsFileTime function


## -description

The 
    <b>GetSystemTimePreciseAsFileTime</b> 
    function retrieves the current system date and time with the highest possible level of precision (&lt;1us). The 
    retrieved information is in Coordinated Universal Time (UTC) format.

## -parameters

### -param lpSystemTimeAsFileTime [out]

Type: <b>LPFILETIME</b>

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the 
      current system date and time in UTC format.

## -remarks

<div class="alert"><b>Note</b>  This function is best suited for high-resolution time-of-day measurements, or time stamps that are synchronized to UTC. For high-resolution interval measurements, use <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a> or <a href="/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter">KeQueryPerformanceCounter</a>. For more info about acquiring high-resolution time stamps, see <a href="/windows/desktop/SysInfo/acquiring-high-resolution-time-stamps">Acquiring high-resolution time stamps</a>.</div>
<div> </div>