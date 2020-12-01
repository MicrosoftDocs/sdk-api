---
UID: NF:wininet.InternetGetCookieEx2
title: InternetGetCookieEx2 function (wininet.h)
description: Retrieves one or more cookies associated with the specified URL.
helpviewer_keywords: ["InternetGetCookieEx2","InternetGetCookieEx2 function [WinINet]","_win32_internetgetcookieex2","wininet.internetgetcookieex2","wininet/InternetGetCookieEx2"]
tech.root: wininet
ms.assetid: b0a45dd2-58be-4178-81ee-bcdc4ff54f84
ms.date: 12/01/2020
ms.keywords: InternetGetCookieEx2, InternetGetCookieEx2 function [WinINet], _win32_internetgetcookieex2, wininet.internetgetcookieex2, wininet/InternetGetCookieEx2
req.header: wininet.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
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
 - InternetGetCookieEx2
 - wininet/InternetGetCookieEx2
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
 - InternetGetCookieEx2
---

# InternetGetCookieEx2 function


## -description

Retrieves one or more cookies associated with the specified URL.

## -parameters

### -param pcwszUrl [in]

The URL for which to retrieve cookies.

### -param pcwszCookieName [in]

The name of the cookie to retrieve. May be NULL.

### -param dwFlags [in]

Flags of the cookie to retrieve. The following flags are available.

| Value | Meaning |
|-|-|
| INTERNET_COOKIE_THIRD_PARTY | Retrieve cookies as a third party, causing first-party-only cookies to be excluded. |
| INTERNET_COOKIE_NON_SCRIPT | Indicate that this query was not triggered via JavaScript, allowing retrieval of HTTP-only cookies. |
| INTERNET_COOKIE_SAME_SITE_LEVEL_CROSS_SITE | Retrieve cookies as if in a cross site context, excluding cookies with the SameSite property set. |
| INTERNET_FLAG_RESTRICTED_ZONE | Retrieve only cookies that would be allowed if the specified URL were untrusted; that is, if it belonged to the URLZONE_UNTRUSTED zone. |

### -param ppCookies [out]

Pointer that receives an array of [INTERNET\_COOKIE2](/windows/desktop/api/wininet/ns-wininet-internet-cookie2) structures. The returned array must be freed by [InternetFreeCookies](/windows/desktop/api/wininet/nf-wininet-internetfreecookies).

### -param pdwCookieCount [out]

Pointer to a DWORD that receives the number of structures in the array.

### -returns

Returns ERROR_SUCCESS if successful, or a [system error code](/windows/desktop/debug/system-error-codes) on failure.


## -remarks

> [!Note]
> WinINet does not support server implementations. In addition, it should not be used from a service. For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/winhttp/winhttp-start-page).


## -see-also

[HTTP Cookies](/windows/desktop/wininet/http-cookies)

[Managing Cookies](/windows/desktop/wininet/managing-cookies)

[InternetSetCookieEx2](/windows/desktop/api/wininet/nf-wininet-internetsetcookieex2)

[InternetFreeCookies](/windows/desktop/api/wininet/nf-wininet-internetfreecookies)

[WinINet Functions](/windows/desktop/wininet/wininet-functions)
