---
UID: NS:wininet.INTERNET_COOKIE2
title: INTERNET_COOKIE2
description: The INTERNET_COOKIE2 structure contains the constituent parts of a cookie. This structure is used with the InternetGetCookieEx2 and InternetSetCookieEx2 functions.
tech.root: wininet
helpviewer_keywords: ["INTERNET_COOKIE2","INTERNET_COOKIE2 structure [WinINet]","_inet_internet_cookie2_structure","wininet.internet_cookie2","wininet/INTERNET_COOKIE2"]
ms.date: 12/03/2020
ms.keywords: __unnamed_struct_37, INTERNET_COOKIE2
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.header: wininet.h
req.include-header: 
req.kmdf-ver: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.target-type: 
req.typenames: INTERNET_COOKIE2
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - INTERNET_COOKIE2
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - __unnamed_struct_37
 - INTERNET_COOKIE2
---

## -description

The **INTERNET\_COOKIE2** contains the constituent parts of a cookie. This structure is used with the [InternetGetCookieEx2](nf-wininet-internetgetcookieex2.md) and [InternetSetCookieEx2](nf-wininet-internetsetcookieex2.md) functions.

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
|-------|---------|
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

> [!NOTE]
> WinINet does not support server implementations. In addition, it should not be used from a service. For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/winhttp/winhttp-start-page).

## -see-also

[InternetGetCookieEx2](nf-wininet-internetgetcookieex2.md)

[InternetSetCookieEx2](nf-wininet-internetsetcookieex2.md)

[InternetFreeCookies](nf-wininet-internetfreecookies.md)

