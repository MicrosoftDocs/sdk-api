---
UID: NF:wininet.InternetFreeCookies
title: InternetFreeCookies function (wininet.h)
description: Frees an array of INTERNET_COOKIE2 structures.
helpviewer_keywords: ["InternetFreeCookies","InternetFreeCookies function [WinINet]","_win32_internetfreecookies","wininet.internetfreecookies","wininet/InternetFreeCookies"]
tech.root: wininet
ms.assetid: deb65fe2-cf7c-42bc-b17f-ac808e037c40
ms.date: 12/01/2020
ms.keywords: InternetFreeCookies, InternetFreeCookies function [WinINet], _win32_internetfreecookies, wininet.internetfreecookies, wininet/InternetFreeCookies
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
 - InternetFreeCookies
 - wininet/InternetFreeCookies
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
 - InternetFreeCookies
---

# InternetFreeCookies function


## -description

Frees an array of [INTERNET\_COOKIE2](/windows/desktop/api/wininet/ns-wininet-internet-cookie2) structures returned by [InternetGetCookieEx2](/windows/desktop/api/wininet/nf-wininet-internetgetcookieex2).

## -parameters

### -param pCookies [in]

Pointer to an array of [**INTERNET\_COOKIE2**](/windows/desktop/api/wininet/ns-wininet-internet-cookie2) structures.

### -param dwCookieCount [in]

The number of structures in the array.


## -remarks

> [!Note]
> WinINet does not support server implementations. In addition, it should not be used from a service. For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/winhttp/winhttp-start-page).


## -see-also

[HTTP Cookies](/windows/desktop/wininet/http-cookies)

[Managing Cookies](/windows/desktop/wininet/managing-cookies)

[InternetGetCookieEx2](/windows/desktop/api/wininet/nf-wininet-internetgetcookieex2)

[InternetSetCookieEx2](/windows/desktop/api/wininet/nf-wininet-internetsetcookieex2)

[WinINet Functions](/windows/desktop/wininet/wininet-functions)
