---
UID: NF:winternl.RtlTimeToSecondsSince1970
title: RtlTimeToSecondsSince1970 function (winternl.h)
description: Converts the specified 64-bit system time to the number of seconds since the beginning of January 1, 1970.
helpviewer_keywords: ["RtlTimeToSecondsSince1970","RtlTimeToSecondsSince1970 function","base.rtltimetosecondssince1970","winternl/RtlTimeToSecondsSince1970"]
old-location: base\rtltimetosecondssince1970.htm
tech.root: winprog
ms.assetid: cb2e041a-cbbb-4572-85da-b282fa692261
ms.date: 12/05/2018
ms.keywords: RtlTimeToSecondsSince1970, RtlTimeToSecondsSince1970 function, base.rtltimetosecondssince1970, winternl/RtlTimeToSecondsSince1970
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlTimeToSecondsSince1970
 - winternl/RtlTimeToSecondsSince1970
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - RtlTimeToSecondsSince1970
---

# RtlTimeToSecondsSince1970 function


## -description

<p class="CCE_Message">[<b>RtlTimeToSecondsSince1970</b> is available for use in Windows 2000 and Windows XP.  It may be unavailable or modified in subsequent releases.]

Converts the specified 64-bit system time to the
    number of seconds since the beginning of January 1, 1970.

## -parameters

### -param Time [in]

A pointer to a <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structure that specifies the system time. The valid years for this value are 1970 to  2105 inclusive.

### -param ElapsedSeconds [out]

A pointer to a variable that receives the number of seconds.

## -returns

If the function succeeds, it returns <b>TRUE</b>. If it fails, it returns <b>FALSE</b>. Typically, this function will fail if the specified value of the  <i>Time</i> parameter is not within the valid timeframe specified in the parameter description.

## -remarks

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Ntdll.dll.

There is no single equivalent public  function. To perform this task using public  functions, use the following steps:



<ol>
<li>Call  <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a> to copy the system time to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure. Call <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemtime">GetSystemTime</a> to get the current system time to pass to <b>SystemTimeToFileTime</b>.</li>
<li>Copy the contents of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure to a <a href="/windows/win32/api/winnt/ns-winnt-ularge_integer-r1">ULARGE_INTEGER</a> structure.</li>
<li>Initialize a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure with the date and time of the first second of January 1, 1970.</li>
<li>Call <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a>, passing the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure initialized in Step 3 to the call.</li>
<li>Copy the contents of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure returned by <a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a> in Step 4 to a second <a href="/windows/win32/api/winnt/ns-winnt-ularge_integer-r1">ULARGE_INTEGER</a>.
The copied value should be less than or equal to the value copied in Step 2.</li>
<li>Subtract the 64-bit value in the <a href="/windows/win32/api/winnt/ns-winnt-ularge_integer-r1">ULARGE_INTEGER</a> structure initialized in Step 5 (January 1, 1970) from the 64-bit value of the <b>ULARGE_INTEGER</b> structure initialized in Step 2 (the current system time). This produces a value in 100-nanosecond intervals since January 1, 1970. To convert this value to seconds, divide by 10,000,000.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>



<a href="/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime">SystemTimeToFileTime</a>



<a href="/windows/desktop/SysInfo/time-functions">Time Functions</a>



<a href="/windows/win32/api/winnt/ns-winnt-ularge_integer-r1">ULARGE_INTEGER</a>