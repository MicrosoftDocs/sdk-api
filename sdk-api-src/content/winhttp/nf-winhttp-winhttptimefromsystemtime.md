---
UID: NF:winhttp.WinHttpTimeFromSystemTime
title: WinHttpTimeFromSystemTime function (winhttp.h)
description: Formats a date and time according to the HTTP version 1.0 specification. (WinHttpTimeFromSystemTime)
helpviewer_keywords: ["WinHttpTimeFromSystemTime","WinHttpTimeFromSystemTime function [WinHTTP]","http.winhttptimefromsystemtime","winhttp.winhttptimefromsystemtime_function","winhttp/WinHttpTimeFromSystemTime"]
old-location: http\winhttptimefromsystemtime.htm
tech.root: http
ms.assetid: 8d55e3bb-0b86-41d9-ba39-62feb2acc707
ms.date: 12/05/2018
ms.keywords: WinHttpTimeFromSystemTime, WinHttpTimeFromSystemTime function [WinHTTP], http.winhttptimefromsystemtime, winhttp.winhttptimefromsystemtime_function, winhttp/WinHttpTimeFromSystemTime
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winhttp.lib
req.dll: Winhttp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.
ms.custom: 19H1
f1_keywords:
 - WinHttpTimeFromSystemTime
 - winhttp/WinHttpTimeFromSystemTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winhttp.dll
api_name:
 - WinHttpTimeFromSystemTime
---

# WinHttpTimeFromSystemTime function


## -description

The <b>WinHttpTimeFromSystemTime</b> function formats a date and time according to the HTTP version 1.0 specification.

## -parameters

### -param pst [in]

A pointer to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date and time to format.

### -param pwszTime [out]

A pointer to a string buffer that receives the formatted date and time. The buffer should equal to the size, in bytes, of WINHTTP_TIME_FORMAT_BUFSIZE.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get  extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Error codes include the following.

<table>
<tr>
<th>Error Code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error has occurred.

</td>
</tr>
</table>

## -remarks

Even when  WinHTTP is used in asynchronous mode (that is, when <b>WINHTTP_FLAG_ASYNC</b> has been set in <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpopen">WinHttpOpen</a>), this function operates synchronously. The return value indicates success or failure.  To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHTTP Start Page.</div>
<div> </div>

#### Examples

The following  code example code shows how to convert a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure to a string that contains the time in HTTP format.


```cpp
    SYSTEMTIME  sTime;
    LPWSTR      pwszTimeStr;

    // Get the current time.
    GetSystemTime(&sTime);

    // Allocate memory for the string.
    // Note: WINHTTP_TIME_FORMAT_BUFSIZE is a byte count.
    //       Therefore, you must divide the array by
    //       sizeof WCHAR to get the proper string length.
    pwszTimeStr = new WCHAR[WINHTTP_TIME_FORMAT_BUFSIZE/sizeof(WCHAR)];

    // Convert the current time to HTTP format.
    if(!WinHttpTimeFromSystemTime( &sTime, pwszTimeStr))
    {
        printf( "Error %u in WinHttpTimeFromSystemTime.\n", GetLastError());
    }
    else
    {
        // Print the time.
        printf("Current time is (%S)\n", pwszTimeStr);
    }

    // Free the memory.
    delete [] pwszTimeStr;

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttptimetosystemtime">WinHttpTimeToSystemTime</a>
