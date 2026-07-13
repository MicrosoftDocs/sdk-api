---
UID: NF:wininet.InternetReadFileExW
title: InternetReadFileExW function (wininet.h)
description: Reads data from a handle opened by the InternetOpenUrl or HttpOpenRequest function. (Unicode)
helpviewer_keywords: ["InternetReadFileEx", "InternetReadFileEx function [WinINet]", "InternetReadFileExW", "_inet_internetreadfileex_function", "wininet.internetreadfileex", "wininet/InternetReadFileEx", "wininet/InternetReadFileExW"]
old-location: wininet\internetreadfileex.htm
tech.root: wininet
ms.assetid: 04e7bb7e-d925-41fd-8333-3cb443a04c5b
ms.date: 12/05/2018
ms.keywords: InternetReadFileEx, InternetReadFileEx function [WinINet], InternetReadFileExA, InternetReadFileExW, _inet_internetreadfileex_function, wininet.internetreadfileex, wininet/InternetReadFileEx, wininet/InternetReadFileExA, wininet/InternetReadFileExW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetReadFileExW (Unicode) and InternetReadFileExA (ANSI)
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
 - InternetReadFileExW
 - wininet/InternetReadFileExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetReadFileEx
 - InternetReadFileExA
 - InternetReadFileExW
---

# InternetReadFileExW function


## -description

Reads data from a handle opened by the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> function.

## -parameters

### -param hFile [in]

Handle returned by the 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopenurla">InternetOpenUrl</a> or 
<a href="/windows/desktop/api/wininet/nf-wininet-httpopenrequesta">HttpOpenRequest</a> function.

### -param lpBuffersOut [out]

Pointer to an 
<a href="/windows/desktop/api/wininet/ns-wininet-internet_buffersa">INTERNET_BUFFERS</a> structure that receives the data downloaded.

### -param dwFlags [in]

This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>IRF_ASYNC</dt>
</dl>
</td>
<td width="60%">
Identical to  <a href="/windows/desktop/WinInet/api-flags">WININET_API_FLAG_ASYNC</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>IRF_SYNC</dt>
</dl>
</td>
<td width="60%">
Identical to <a href="/windows/desktop/WinInet/api-flags">WININET_API_FLAG_SYNC</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>IRF_USE_CONTEXT</dt>
</dl>
</td>
<td width="60%">
Identical to <a href="/windows/desktop/WinInet/api-flags">WININET_API_FLAG_USE_CONTEXT</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>IRF_NO_WAIT</dt>
</dl>
</td>
<td width="60%">
Do not wait for data. If there is data available, the function returns either the amount of data requested or the amount of data available (whichever is smaller).

</td>
</tr>
</table>

### -param dwContext [in]

A caller supplied context value used for asynchronous operations.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. An application can also use 
<a href="/windows/desktop/api/wininet/nf-wininet-internetgetlastresponseinfoa">InternetGetLastResponseInfo</a> when necessary.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetReadFileEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/common-functions">Common Functions</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
