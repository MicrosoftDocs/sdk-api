---
UID: NF:wininet.InternetTimeFromSystemTimeW
title: InternetTimeFromSystemTimeW function (wininet.h)
description: The InternetTimeFromSystemTimeW (Unicode) function (wininet.h) formats a date and time according to the HTTP version 1.0 specification.
helpviewer_keywords: ["InternetTimeFromSystemTime", "InternetTimeFromSystemTime function [WinINet]", "InternetTimeFromSystemTimeW", "_inet_internettimefromsystemtime_function", "wininet.internettimefromsystemtime", "wininet/InternetTimeFromSystemTime", "wininet/InternetTimeFromSystemTimeW"]
old-location: wininet\internettimefromsystemtime.htm
tech.root: wininet
ms.assetid: b52ba402-bad1-4005-b9d0-7630194272d1
ms.date: 08/10/2022
ms.keywords: InternetTimeFromSystemTime, InternetTimeFromSystemTime function [WinINet], InternetTimeFromSystemTimeA, InternetTimeFromSystemTimeW, _inet_internettimefromsystemtime_function, wininet.internettimefromsystemtime, wininet/InternetTimeFromSystemTime, wininet/InternetTimeFromSystemTimeA, wininet/InternetTimeFromSystemTimeW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetTimeFromSystemTimeW (Unicode) and InternetTimeFromSystemTimeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetTimeFromSystemTimeW
 - wininet/InternetTimeFromSystemTimeW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
 - API-MS-Win-Http-Time-l1-1-0.dll
 - KernelBase.dll
api_name:
 - InternetTimeFromSystemTime
 - InternetTimeFromSystemTimeA
 - InternetTimeFromSystemTimeW
---

# InternetTimeFromSystemTimeW function


## -description

Formats a date and time according to the HTTP version 1.0 specification.

## -parameters

### -param pst [in]

Pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date and time to format.

### -param dwRFC [in]

RFC format used. Currently, the only valid format is INTERNET_RFC1123_FORMAT.

### -param lpszTime [out]

Pointer to a string buffer that receives the formatted date and time. The buffer should be of size INTERNET_RFC1123_BUFSIZE.

### -param cbTime [in]

Size of the 
<i>lpszTime</i> buffer, in bytes.

## -returns

Returns TRUE if the function succeeds, or FALSE otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetTimeFromSystemTime as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
