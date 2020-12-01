---
UID: NF:wininet.InternetGetCookieEx2
title: InternetGetCookieEx2 function (wininet.h)
description: Creates a cookie associated with the specified URL.
helpviewer_keywords: ["InternetSetCookieEx2","InternetSetCookieEx2 function [WinINet]","_win32_internetsetcookieex2","wininet.internetsetcookieex2","wininet/InternetSetCookieEx2"]
tech.root: wininet
ms.assetid: c13ed369-0844-470c-8793-82f95a240c1b
ms.date: 12/01/2020
ms.keywords: InternetSetCookieEx2, InternetSetCookieEx2 function [WinINet], _win32_internetsetcookieex2, wininet.internetsetcookieex2, wininet/InternetSetCookieEx2
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
 - InternetSetCookieEx2
 - wininet/InternetSetCookieEx2
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
 - InternetSetCookieEx2
---

# InternetSetCookieEx2 function


## -description

Creates a cookie associated with the specified URL.

## -parameters

### -param pcwszUrl [in]

The URL for which to set the cookie.

### -param pCookie [in]

Pointer to an [INTERNET\_COOKIE2](/windows/desktop/api/wininet/ns-wininet-internet-cookie2) structure containing the cookie data.

### -param pcwszP3PPolicy [in]

String containing the Platform-for-Privacy-Protection (P3P) policy for the cookie. May be NULL.

### -param dwFlags [in]

Flags for the cookie to be set. The following flags are available.

| Value | Meaning |
|-|-|
| INTERNET_COOKIE_THIRD_PARTY | Set this cookie in a third-party context. |
| INTERNET_COOKIE_PROMPT_REQUIRED | Show a UI prompt for the user to accept or reject this cookie. |
| INTERNET_COOKIE_EVALUATE_P3P | Evaluate the provided P3P policy for this cookie. This will evaluate default policy when *pcwszP3PPolicy* is NULL. |
| INTERNET_COOKIE_NON_SCRIPT | Indicate that this cookie is not being set via JavaScript, allowing HTTP-only cookies to be set. |
| INTERNET_COOKIE_APPLY_HOST_ONLY | Apply host-only policy to this cookie. If the domain attribute is not set, then this cookie will be marked host-only. |

### -param pdwCookieState [out]

Pointer to a DWORD that receives the result of setting the cookie. For a list of possible values, see [InternetCookieState](/windows/desktop/wininet/ne-wininet.internetcookiestate).

### -returns

Returns ERROR_SUCCESS if successful, or a [system error code](/windows/desktop/debug/system-error-codes) on failure.


## -remarks

> [!Note]
> WinINet does not support server implementations. In addition, it should not be used from a service. For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/winhttp/winhttp-start-page).


## -see-also

[HTTP Cookies](/windows/desktop/wininet/http-cookies)

[Managing Cookies](/windows/desktop/wininet/managing-cookies)

[InternetGetCookieEx2](/windows/desktop/api/wininet/nf-wininet-internetgetcookieex2)

[InternetFreeCookies](/windows/desktop/api/wininet/nf-wininet-internetfreecookies)

[WinINet Functions](/windows/desktop/wininet/wininet-functions)
