---
UID: NF:winhttp.WinHttpTimeToSystemTime
title: WinHttpTimeToSystemTime function (winhttp.h)
description: The WinHttpTimeToSystemTime function takes an HTTP time/date string and converts it to a SYSTEMTIME structure.
helpviewer_keywords: ["WinHttpTimeToSystemTime","WinHttpTimeToSystemTime function [WinHTTP]","http.winhttptimetosystemtime","winhttp.winhttptimetosystemtime_function","winhttp/WinHttpTimeToSystemTime"]
old-location: http\winhttptimetosystemtime.htm
tech.root: http
ms.assetid: 4a587832-e1ce-42d4-97bb-a728f895906b
ms.date: 12/05/2018
ms.keywords: WinHttpTimeToSystemTime, WinHttpTimeToSystemTime function [WinHTTP], http.winhttptimetosystemtime, winhttp.winhttptimetosystemtime_function, winhttp/WinHttpTimeToSystemTime
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
 - WinHttpTimeToSystemTime
 - winhttp/WinHttpTimeToSystemTime
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
 - WinHttpTimeToSystemTime
---

# WinHttpTimeToSystemTime function


## -description

The <b>WinHttpTimeToSystemTime</b> function takes an HTTP time/date string and converts it to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.

## -parameters

### -param pwszTime [in]

Pointer to a null-terminated date/time string to convert. This value must use the format defined in section 3.3 of the <a href="http://www.ietf.org/rfc/rfc2616.txt">RFC2616</a>.

### -param pst [out]

Pointer to the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that receives the converted time.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Among the error codes returned is:

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

<div class="alert"><b>Note</b>  For Windows XP and Windows 2000, see the <a href="/windows/desktop/WinHttp/winhttp-start-page">Run-Time Requirements</a> section of the WinHttp start page.</div>
<div> </div>

#### Examples

This example shows how to convert an HTTP formatted date to a 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.


```cpp
    SYSTEMTIME  sTime;
    LPCWSTR     pwszTimeStr = L"Tue, 21 Nov 2000 01:06:53 GMT";

    // Convert the HTTP string to a SYSTEMTIME structure.
    if (!WinHttpTimeToSystemTime( pwszTimeStr, &sTime))
    {
        printf( "Error %u in WinHttpTimeToSystemTime.\n", GetLastError());
    }
    else
    {
        // Print the date.
        printf( "The U.S. formatted date is (%u/%u/%u)\n", 
                sTime.wMonth, sTime.wDay, sTime.wYear);
    }

```

## -see-also

<a href="/windows/desktop/WinHttp/about-winhttp">About Microsoft Windows HTTP Services (WinHTTP)</a>



<a href="/windows/desktop/WinHttp/winhttp-versions">WinHTTP Versions</a>



<a href="/windows/desktop/api/winhttp/nf-winhttp-winhttptimefromsystemtime">WinHttpTimeFromSystemTime</a>