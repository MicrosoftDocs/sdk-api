---
UID: NS:wininet.INTERNET_COOKIE2
title: INTERNET_COOKIE2 (wininet.h)
description: The INTERNET_COOKIE2 structure contains the constituent parts of a cookie. This structure is used with the InternetGetCookieEx2 and InternetSetCookieEx2 functions.
helpviewer_keywords: ["INTERNET_COOKIE2","INTERNET_COOKIE2 structure [WinINet]","_inet_internet_cookie2_structure","wininet.internet_cookie2","wininet/INTERNET_COOKIE2"]
tech.root: wininet
ms.assetid: 7998f2da-34d2-412c-824f-253b787754a4
ms.date: 12/01/2020
ms.keywords: 'INTERNET_COOKIE2, INTERNET_COOKIE2 structure [WinINet], _inet_internet_cookie2_structure, wininet.internet_cookie2, wininet/INTERNET_COOKIE2'
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
req.lib:
req.dll:
req.irql:
targetos: Windows
req.typenames: INTERNET_COOKIE2
req.redist:
ms.custom: 19H1
f1_keywords:
 - INTERNET_COOKIE2
 - wininet/INTERNET_COOKIE2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wininet.h
api_name:
 - INTERNET_COOKIE2
---

# INTERNET_COOKIE2 structure


## -description

The **INTERNET\_COOKIE2** contains the constituent parts of a cookie. This structure is used with the [InternetGetCookieEx2](/windows/desktop/api/wininet/nf-wininet-internetgetcookieex2) and [InternetSetCookieEx2](/windows/desktop/api/wininet/nf-wininet-internetsetcookieex2) functions.

## -struct-fields

### -field pwszName

Pointer to a string containing the cookie name. May be NULL if value is not NULL.

### -field pwszValue

Pointer to a string containing the cookie value. May be NULL if name is not NULL.

### -field pwszDomain

Pointer to a string containing the cookie domain. May be NULL.

### -field pwszPath

Pointer to a string containing the cookie path. May be NULL.

### -field dwFlags

Flags for additional cookie details. The following flags are available.

| Value | Meaning |
|-|-|
| INTERNET_COOKIE_IS_SECURE | This is a secure cookie. |
| INTERNET_COOKIE_IS_SESSION | This is a session cookie. |
| INTERNET_COOKIE_IS_RESTRICTED | This cookie is restricted to first-party contexts. |
| INTERNET_COOKIE_HTTPONLY | This is an HTTP-only cookie. |
| INTERNET_COOKIE_HOST_ONLY | This is a host-only cookie. |
| INTERNET_COOKIE_HOST_ONLY_APPLIED | The host-only setting has been applied to this cookie. |
| INTERNET_COOKIE_SAME_SITE_STRICT | The SameSite security level for this cookie is "strict". |
| INTERNET_COOKIE_SAME_SITE_LAX | The SameSite security level for this cookie is "lax". |

### -field ftExpires

The expiry time of the cookie.

### -field fExpiresSet

Whether or not the expiry time is set.


## -remarks

> [!Note]
> WinINet does not support server implementations. In addition, it should not be used from a service. For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/winhttp/winhttp-start-page).


## -see-also

[InternetGetCookieEx2](/windows/desktop/api/wininet/nf-wininet-internetgetcookieex2)

[InternetSetCookieEx2](/windows/desktop/api/wininet/nf-wininet-internetsetcookieex2)

[InternetFreeCookies](/windows/desktop/api/wininet/nf-wininet-internetfreecookies)
