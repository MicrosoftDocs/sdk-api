---
UID: NF:wininet.InternetCreateUrlA
title: InternetCreateUrlA function (wininet.h)
description: Creates a URL from its component parts. (ANSI)
helpviewer_keywords: ["InternetCreateUrlA", "wininet/InternetCreateUrlA"]
old-location: wininet\internetcreateurl.htm
tech.root: wininet
ms.assetid: b01bb684-0b2f-4c17-ab32-9f83fdd89e69
ms.date: 12/05/2018
ms.keywords: InternetCreateUrl, InternetCreateUrl function [WinINet], InternetCreateUrlA, InternetCreateUrlW, _inet_internetcreateurl_function, wininet.internetcreateurl, wininet/InternetCreateUrl, wininet/InternetCreateUrlA, wininet/InternetCreateUrlW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetCreateUrlW (Unicode) and InternetCreateUrlA (ANSI)
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
 - InternetCreateUrlA
 - wininet/InternetCreateUrlA
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
 - InternetCreateUrl
 - InternetCreateUrlA
 - InternetCreateUrlW
---

# InternetCreateUrlA function


## -description

Creates a URL from its component parts.

## -parameters

### -param lpUrlComponents [in]

Pointer to a 
<a href="/windows/desktop/api/wininet/ns-wininet-url_componentsa">URL_COMPONENTS</a> structure that contains the components from which to create the URL.

### -param dwFlags [in]

Controls the operation of this function. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ICU_ESCAPE</dt>
</dl>
</td>
<td width="60%">
Converts all unsafe characters to their corresponding escape sequences in the path string pointed to by the <b>lpszUrlPath</b> member and in <b>lpszExtraInfo</b> the extra-information string pointed to by the member of the <a href="/windows/desktop/api/wininet/ns-wininet-url_componentsa">URL_COMPONENTS</a> structure pointed to by the <i>lpUrlComponents</i> parameter.

The Unicode version of <b>InternetCreateUrl</b> will first try to convert using the system code page.  If that fails it falls back to UTF-8.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>ICU_USERNAME</dt>
</dl>
</td>
<td width="60%">
Obsolete — ignored.

</td>
</tr>
</table>

### -param lpszUrl [out]

Pointer to a buffer that receives the URL.

### -param lpdwUrlLength [in, out]

Pointer to a variable that specifies the size of the 
URL <i>lpszUrl</i> buffer, in <b>TCHARs</b>. When the function returns, this parameter receives the size of the URL string, excluding the NULL terminator. If 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, this parameter receives the number of bytes required to hold the created URL.

## -returns

Returns <b>TRUE</b> if the function succeeds, or <b>FALSE</b> otherwise. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When specifying scheme in the <a href="/windows/desktop/api/wininet/ns-wininet-url_componentsa">URL_COMPONENTS</a> structure passed to <i>lpUrlComponents</i>, if <i>lpszScheme</i> is not NULL it will be used for the scheme.  If <i>lpszScheme</i> is NULL, the scheme can be specified using the <a href="/windows/desktop/api/wininet/ne-wininet-internet_scheme">INTERNET_SCHEME</a> enumeration by setting <b>nScheme</b> to the required <b>INTERNET_SCHEME</b> or <b>INTERNET_SCHEME_DEFAULT</b>.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetCreateUrl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/handling-uniform-resource-locators">Handling Uniform Resource Locators</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
