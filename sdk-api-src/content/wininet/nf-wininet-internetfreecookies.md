---
UID: NF:wininet.InternetFreeCookies
title: InternetFreeCookies
description: Frees an array of INTERNET_COOKIE2 structures.
helpviewer_keywords: ["InternetFreeCookies","InternetFreeCookies function [WinINet]","_win32_internetfreecookies","wininet.internetfreecookies","wininet/InternetFreeCookies"]
tech.root: wininet
ms.date: 12/03/2020
ms.keywords: InternetFreeCookies
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
 - InternetFreeCookies
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetFreeCookies
---

## -description

Frees an array of [INTERNET\_COOKIE2](ns-wininet-internet_cookie2.md) structures returned by [InternetGetCookieEx2](nf-wininet-internetgetcookieex2.md).

## -parameters

### -param pCookies

Pointer to an array of [**INTERNET\_COOKIE2**](ns-wininet-internet_cookie2.md) structures.

### -param dwCookieCount

The number of structures in the array.

## -remarks

> [!NOTE]
> WinINet does not support server implementations. In addition, it should not be used from a service. For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/winhttp/winhttp-start-page).

## -see-also

[HTTP Cookies](/windows/win32/wininet/http-cookies)

[Managing Cookies](/windows/win32/wininet/managing-cookies)

[InternetGetCookieEx2](nf-wininet-internetgetcookieex2.md)

[InternetSetCookieEx2](nf-wininet-internetsetcookieex2.md)

[WinINet Functions](/windows/win32/wininet/wininet-functions)
