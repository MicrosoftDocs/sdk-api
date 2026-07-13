---
UID: NF:wininet.InternetGetCookieA
title: InternetGetCookieA function (wininet.h)
description: Retrieves the cookie for the specified URL. (ANSI)
helpviewer_keywords: ["InternetGetCookieA", "wininet/InternetGetCookieA"]
old-location: wininet\internetgetcookie.htm
tech.root: wininet
ms.assetid: 12c1ebab-3954-4995-9e1f-bf29699af396
ms.date: 12/05/2018
ms.keywords: InternetGetCookie, InternetGetCookie function [WinINet], InternetGetCookieA, InternetGetCookieW, _win32_internetgetcookie, wininet.internetgetcookie, wininet/InternetGetCookie, wininet/InternetGetCookieA, wininet/InternetGetCookieW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetGetCookieW (Unicode) and InternetGetCookieA (ANSI)
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
 - InternetGetCookieA
 - wininet/InternetGetCookieA
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
 - InternetGetCookie
 - InternetGetCookieA
 - InternetGetCookieW
---

# InternetGetCookieA function


## -description

Retrieves the cookie for the specified URL.

## -parameters

### -param lpszUrl [in]

A pointer to a <b>null</b>-terminated string that specifies the URL for which cookies are to be retrieved.

### -param lpszCookieName [in]

Not implemented.

### -param lpszCookieData [out]

A pointer to a buffer that receives the cookie data. This parameter can be <b>NULL</b>.

### -param lpdwSize [in, out]

A pointer to a variable that specifies the size of the 
<i>lpszCookieData</i> parameter buffer, in TCHARs. If the function succeeds, the buffer receives the amount of data copied to the 
<i>lpszCookieData</i> buffer. If 
<i>lpszCookieData</i> is <b>NULL</b>, this parameter receives a value that specifies the size of the buffer necessary to copy all the cookie data, expressed as a byte count.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.


If the function fails, it returns <b>FALSE</b>. To get extended error data, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error values apply to 
<b>InternetGetCookie</b>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There is no cookie for the specified URL and all its parents.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The value passed in 
<i>lpdwSize</i> is insufficient to copy all the cookie data. The value returned in 
<i>lpdwSize</i> is the size of the buffer necessary to get all the data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is invalid.

The <i>lpszUrl</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<b>InternetGetCookie</b> does not require a call to 
<a href="/windows/desktop/api/wininet/nf-wininet-internetopena">InternetOpen</a>. 
<b>InternetGetCookie</b> checks in the windows\cookies directory for persistent cookies that have an expiration date set sometime in the future. 
<b>InternetGetCookie</b> also searches memory for any session cookies, that is, cookies that do not have an expiration date that were created in the same process by 
<a href="/windows/desktop/api/wininet/nf-wininet-internetsetcookiea">InternetSetCookie</a>, because these cookies are not written to any files. Rules for creating cookie files are internal to the system and can change in the future.

As noted in <a href="/windows/desktop/WinInet/http-cookies">HTTP Cookies</a>, <b>InternetGetCookie</b> does not return cookies that the server marked as non-scriptable with the "HttpOnly" attribute in the Set-Cookie header.

Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetGetCookie as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/http-cookies">HTTP Cookies</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetgetcookieexa">InternetGetCookieEx</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetcookiea">InternetSetCookie</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetcookieexa">InternetSetCookieEx</a>



<a href="/windows/desktop/WinInet/managing-cookies">Managing Cookies</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
