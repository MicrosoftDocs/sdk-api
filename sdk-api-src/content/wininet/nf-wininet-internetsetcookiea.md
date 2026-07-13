---
UID: NF:wininet.InternetSetCookieA
title: InternetSetCookieA function (wininet.h)
description: Creates a cookie associated with the specified URL. (InternetSetCookieA)
helpviewer_keywords: ["InternetSetCookieA", "wininet/InternetSetCookieA"]
old-location: wininet\internetsetcookie.htm
tech.root: wininet
ms.assetid: 1b1ca72e-9c74-4e94-86a9-6fee12c83933
ms.date: 12/05/2018
ms.keywords: InternetSetCookie, InternetSetCookie function [WinINet], InternetSetCookieA, InternetSetCookieW, _win32_internetsetcookie, wininet.internetsetcookie, wininet/InternetSetCookie, wininet/InternetSetCookieA, wininet/InternetSetCookieW
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InternetSetCookieW (Unicode) and InternetSetCookieA (ANSI)
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
 - InternetSetCookieA
 - wininet/InternetSetCookieA
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
 - InternetSetCookie
 - InternetSetCookieA
 - InternetSetCookieW
---

# InternetSetCookieA function


## -description

Creates a cookie associated with the specified URL.

## -parameters

### -param lpszUrl [in]

Pointer to a <b>null</b>-terminated string that specifies the URL for which the cookie should be set.

### -param lpszCookieName [in]

Pointer to a <b>null</b>-terminated string that specifies the name to be associated with the cookie data. If this parameter is <b>NULL</b>, no name is associated with the cookie.

### -param lpszCookieData [in]

Pointer to the actual data to be associated with the URL.

## -returns

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise. To get a specific error message, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Cookies created by 
<b>InternetSetCookie</b> without an expiration date are stored in memory and are available only in the same process that created them. Cookies that include an expiration date are stored in the windows\cookies directory.

Creating a new cookie might cause a dialog box to appear on the screen asking the user if they want to allow or disallow  cookies from this site based on the privacy settings for the user.


<div class="alert"><b>Caution</b>  <b>InternetSetCookie</b> will unconditionally create a cookie even if “Block all cookies” is set in Internet Explorer. This behavior can be viewed as a breach of privacy even though such cookies are not subsequently sent back to servers while the “Block all cookies” setting is active. Applications should use <a href="/windows/desktop/api/wininet/nf-wininet-internetsetcookieexa">InternetSetCookieEx</a> to correctly honor the user's privacy settings.

<p class="note">For more cookie internals, see <a href="/archive/blogs/ieinternals/">http://blogs.msdn.com/ieinternals/archive/2009/08/20/WinINET-IE-Cookie-Internals-FAQ.aspx</a>.

</div>
<div> </div>


Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>




> [!NOTE]
> The wininet.h header defines InternetSetCookie as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/http-cookies">HTTP Cookies</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetgetcookiea">InternetGetCookie</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetgetcookieexa">InternetGetCookieEx</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetcookieexa">InternetSetCookieEx</a>



<a href="/windows/desktop/WinInet/managing-cookies">Managing Cookies</a>



<a href="/windows/desktop/WinInet/wininet-functions">WinINet Functions</a>
