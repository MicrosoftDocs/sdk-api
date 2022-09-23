---
UID: NF:wininet.InternetSetCookieEx2
title: InternetSetCookieEx2
description: Creates a cookie associated with the specified URL. (InternetSetCookieEx2)
helpviewer_keywords: ["InternetSetCookieEx2","InternetSetCookieEx2 function [WinINet]","_win32_internetsetcookieex2","wininet.internetsetcookieex2","wininet/InternetSetCookieEx2"]
tech.root: wininet
ms.date: 12/03/2020
ms.keywords: InternetSetCookieEx2
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
 - InternetSetCookieEx2
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetSetCookieEx2
---

## -description

Creates a cookie associated with the specified URL.

## -parameters

### -param pcwszUrl

The URL for which to set the cookie.

### -param pCookie

Pointer to an [INTERNET\_COOKIE2](ns-wininet-internet_cookie2.md) structure containing the cookie data.

### -param pcwszP3PPolicy

String containing the Platform-for-Privacy-Protection (P3P) policy for the cookie. May be NULL.

### -param dwFlags

Flags for the cookie to be set. The following flags are available.

| Value | Meaning |
|-------|---------|
| INTERNET_COOKIE_THIRD_PARTY | Set this cookie in a third-party context. |
| INTERNET_COOKIE_PROMPT_REQUIRED | Show a UI prompt for the user to accept or reject this cookie. |
| INTERNET_COOKIE_EVALUATE_P3P | Evaluate the provided P3P policy for this cookie. This will evaluate default policy when *pcwszP3PPolicy* is NULL. |
| INTERNET_COOKIE_NON_SCRIPT | Indicate that this cookie is not being set via JavaScript, allowing HTTP-only cookies to be set. |
| INTERNET_COOKIE_APPLY_HOST_ONLY | Apply host-only policy to this cookie. If the domain attribute is not set, then this cookie will be marked host-only. |

### -param pdwCookieState

Pointer to a DWORD that receives the result of setting the cookie. For a list of possible values, see [InternetCookieState](/windows/win32/api/wininet/ne-wininet-internetcookiestate).

## -returns

Returns ERROR_SUCCESS if successful, or a [system error code](/windows/desktop/debug/system-error-codes) on failure.

## -remarks

> [!NOTE]
> WinINet does not support server implementations. In addition, it should not be used from a service. For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/winhttp/winhttp-start-page).

## -see-also

[HTTP Cookies](/windows/win32/wininet/http-cookies)

[Managing Cookies](/windows/win32/wininet/managing-cookies)

[InternetGetCookieEx2](nf-wininet-internetgetcookieex2.md)

[InternetFreeCookies](nf-wininet-internetfreecookies.md)

[WinINet Functions](/windows/win32/wininet/wininet-functions)
