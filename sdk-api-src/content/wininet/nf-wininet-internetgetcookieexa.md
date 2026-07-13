---
UID: NF:wininet.InternetGetCookieExA
title: InternetGetCookieExA function (wininet.h)
description: Retrieves data stored in cookies associated with a specified URL. (ANSI)
helpviewer_keywords: ["INTERNET_COOKIE_HTTPONLY", "INTERNET_COOKIE_THIRD_PARTY", "INTERNET_FLAG_RESTRICTED_ZONE", "InternetGetCookieExA", "wininet/InternetGetCookieExA"]
old-location: wininet\internetgetcookieex.htm
tech.root: wininet
ms.assetid: 5006f009-e217-4fdc-9e4e-800ff5fcbf03
ms.date: 12/05/2018
ms.keywords: INTERNET_COOKIE_HTTPONLY, INTERNET_COOKIE_THIRD_PARTY, INTERNET_FLAG_RESTRICTED_ZONE, InternetGetCookieEx, InternetGetCookieEx function [WinINet], InternetGetCookieExA, InternetGetCookieExW, wininet.internetgetcookieex, wininet/InternetGetCookieEx, wininet/InternetGetCookieExA, wininet/InternetGetCookieExW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetGetCookieExW (Unicode) and InternetGetCookieExA (ANSI)
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
 - InternetGetCookieExA
 - wininet/InternetGetCookieExA
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
 - InternetGetCookieEx
 - InternetGetCookieExA
 - InternetGetCookieExW
---

# InternetGetCookieExA function


## -description

The <b>InternetGetCookieEx</b> function retrieves data stored in cookies associated with a specified URL. Unlike <a href="/windows/desktop/api/wininet/nf-wininet-internetgetcookiea">InternetGetCookie</a>, <b>InternetGetCookieEx</b> can be used to  restrict data retrieved to a single cookie name or, by policy, associated with untrusted sites or third-party cookies.

## -parameters

### -param lpszUrl [in]

A pointer to a <b>null</b>-terminated string that contains the URL with which the cookie to retrieve is associated. This parameter cannot be <b>NULL</b> or <b>InternetGetCookieEx</b> fails and returns an  <b>ERROR_INVALID_PARAMETER</b> error.

### -param lpszCookieName [in]

A pointer to a <b>null</b>-terminated string that contains the name of the cookie to retrieve. This name is case-sensitive.

### -param lpszCookieData [in, out, optional]

A pointer to a buffer to receive the cookie data.

### -param lpdwSize [in, out]

A pointer to a DWORD variable. 

On entry, the variable must contain the size, in TCHARs, of the buffer pointed to by the <i>pchCookieData</i> parameter.

On exit, if the function is successful, this variable contains the number of TCHARs of cookie data copied into the buffer. If <b>NULL</b> was passed as the <i>lpszCookieData</i> parameter, or if the function fails with an error of <b>ERROR_INSUFFICIENT_BUFFER</b>, the variable contains the size, in BYTEs, of buffer required to receive the cookie data.

This parameter cannot be <b>NULL</b> or <b>InternetGetCookieEx</b> fails and returns an  <b>ERROR_INVALID_PARAMETER</b> error.

### -param dwFlags [in]

A flag that controls how the function retrieves cookie data. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERNET_COOKIE_HTTPONLY"></a><a id="internet_cookie_httponly"></a><dl>
<dt><b>INTERNET_COOKIE_HTTPONLY</b></dt>
</dl>
</td>
<td width="60%">
Enables the retrieval of cookies that are marked as "HTTPOnly".  



Do  not use this flag if you expose a scriptable interface, because this has security implications. It is imperative that you use this flag only if you can guarantee that you will never expose the cookie to third-party code by way of an extensibility mechanism you provide.


<b>Version:  </b>Requires Internet Explorer 8.0 or later.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_COOKIE_THIRD_PARTY"></a><a id="internet_cookie_third_party"></a><dl>
<dt><b>INTERNET_COOKIE_THIRD_PARTY</b></dt>
</dl>
</td>
<td width="60%">
Retrieves only third-party cookies if policy explicitly allows all cookies for the specified URL to be retrieved.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERNET_FLAG_RESTRICTED_ZONE"></a><a id="internet_flag_restricted_zone"></a><dl>
<dt><b>INTERNET_FLAG_RESTRICTED_ZONE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves only cookies that would be allowed if the specified URL were untrusted; that is, if it belonged to the URLZONE_UNTRUSTED zone.

</td>
</tr>
</table>

### -param lpReserved [in]

Reserved for future use. Set to <b>NULL</b>.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. To get a specific error value, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If <b>NULL</b> is passed to <i>lpszCookieData</i>, the call will succeed and the function will not set <b>ERROR_INSUFFICIENT_BUFFER</b>.


The following error codes may be set by this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Returned if cookie data retrieved is larger than the buffer size pointed to by the <i>pcchCookieData</i> parameter or if that parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Returned if either the <i>pchURL</i> or the <i>pcchCookieData</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
Returned if no cookied data as specified could be retrieved.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetGetCookieEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/http-cookies">HTTP Cookies</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetgetcookiea">InternetGetCookie</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetcookiea">InternetSetCookie</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetcookieexa">InternetSetCookieEx</a>



<a href="/windows/desktop/WinInet/managing-cookies">Managing Cookies</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
