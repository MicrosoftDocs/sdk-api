---
UID: NF:wininet.InternetGetCookieEx2
title: InternetGetCookieEx2
description: Retrieves one or more cookies associated with the specified URL.
helpviewer_keywords: ["InternetGetCookieEx2","InternetGetCookieEx2 function [WinINet]","_win32_internetgetcookieex2","wininet.internetgetcookieex2","wininet/InternetGetCookieEx2"]
tech.root: wininet
ms.date: 12/03/2020
ms.keywords: InternetGetCookieEx2
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.header: wininet.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Wininet.lib
req.dll: Wininet.dll 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - InternetGetCookieEx2
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetGetCookieEx2
---

## -description

Retrieves one or more cookies associated with the specified URL.

## -parameters

### -param pcwszUrl

The URL for which to retrieve cookies.

### -param pcwszCookieName

The name of the cookie to retrieve. May be NULL.

### -param dwFlags

Flags of the cookie to retrieve. The following flags are available.

| Value | Meaning |
|-------|---------|
| INTERNET_COOKIE_THIRD_PARTY | Retrieve cookies as a third party, causing first-party-only cookies to be excluded. |
| INTERNET_COOKIE_NON_SCRIPT | Indicate that this query was not triggered via JavaScript, allowing retrieval of HTTP-only cookies. |
| INTERNET_COOKIE_SAME_SITE_LEVEL_CROSS_SITE | Retrieve cookies as if in a cross site context, excluding cookies with the SameSite property set. |
| INTERNET_FLAG_RESTRICTED_ZONE | Retrieve only cookies that would be allowed if the specified URL were untrusted; that is, if it belonged to the URLZONE_UNTRUSTED zone. |

### -param ppCookies

Pointer that receives an array of [INTERNET\_COOKIE2](ns-wininet-internet_cookie2.md) structures. The returned array must be freed by [InternetFreeCookies](nf-wininet-internetfreecookies.md).

### -param pdwCookieCount

Pointer to a DWORD that receives the number of structures in the array.

## -returns

Returns ERROR_SUCCESS if successful, or a [system error code](/windows/desktop/debug/system-error-codes) on failure.

## -remarks

> [!NOTE]
> WinINet does not support server implementations. In addition, it should not be used from a service. For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/winhttp/winhttp-start-page).

## -see-also

[HTTP Cookies](/windows/win32/wininet/http-cookies)

[Managing Cookies](/windows/win32/wininet/managing-cookies)

[InternetSetCookieEx2](nf-wininet-internetsetcookieex2.md)

[InternetFreeCookies](nf-wininet-internetfreecookies.md)

[WinINet Functions](/windows/win32/wininet/wininet-functions)
