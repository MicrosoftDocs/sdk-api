---
UID: NE:wininet.__unnamed_enum_1
title: InternetCookieState (wininet.h)
description: The InternetCookieState enumeration defines the state of the cookie.
helpviewer_keywords: ["COOKIE_STATE_ACCEPT","COOKIE_STATE_DOWNGRADE","COOKIE_STATE_LEASH","COOKIE_STATE_MAX","COOKIE_STATE_PROMPT","COOKIE_STATE_REJECT","COOKIE_STATE_UNKNOWN","InternetCookieState","InternetCookieState enumeration [WinINet]","wininet.internetcookiestate","wininet/COOKIE_STATE_ACCEPT","wininet/COOKIE_STATE_DOWNGRADE","wininet/COOKIE_STATE_LEASH","wininet/COOKIE_STATE_MAX","wininet/COOKIE_STATE_PROMPT","wininet/COOKIE_STATE_REJECT","wininet/COOKIE_STATE_UNKNOWN","wininet/InternetCookieState"]
old-location: wininet\internetcookiestate.htm
tech.root: wininet
ms.assetid: 3f43f492-3133-4cbd-9ab9-3c9600ef5263
ms.date: 12/05/2018
ms.keywords: COOKIE_STATE_ACCEPT, COOKIE_STATE_DOWNGRADE, COOKIE_STATE_LEASH, COOKIE_STATE_MAX, COOKIE_STATE_PROMPT, COOKIE_STATE_REJECT, COOKIE_STATE_UNKNOWN, InternetCookieState, InternetCookieState enumeration [WinINet], wininet.internetcookiestate, wininet/COOKIE_STATE_ACCEPT, wininet/COOKIE_STATE_DOWNGRADE, wininet/COOKIE_STATE_LEASH, wininet/COOKIE_STATE_MAX, wininet/COOKIE_STATE_PROMPT, wininet/COOKIE_STATE_REJECT, wininet/COOKIE_STATE_UNKNOWN, wininet/InternetCookieState
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: InternetCookieState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InternetCookieState
 - wininet/InternetCookieState
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
 - InternetCookieState
---

# InternetCookieState enumeration


## -description

The <b>InternetCookieState</b> enumeration defines the state of the cookie.

## -enum-fields

### -field COOKIE_STATE_UNKNOWN:0x0

Reserved.

### -field COOKIE_STATE_ACCEPT:0x1

The cookies are accepted.

### -field COOKIE_STATE_PROMPT:0x2

The user is prompted to accept or deny the cookie.

### -field COOKIE_STATE_LEASH:0x3

Cookies are accepted only in the first-party context.

### -field COOKIE_STATE_DOWNGRADE:0x4

Cookies are accepted and become session cookies.

### -field COOKIE_STATE_REJECT:0x5

The cookies are rejected.

### -field COOKIE_STATE_MAX

Same as <b>COOKIE_STATE_REJECT</b>.

## -remarks

<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="/windows/desktop/WinHttp/winhttp-start-page">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wininet/nf-wininet-internetenumpersitecookiedecisiona">InternetEnumPerSiteCookieDecision</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetgetpersitecookiedecisiona">InternetGetPerSiteCookieDecision</a>



<a href="/windows/desktop/api/wininet/nf-wininet-internetsetpersitecookiedecisiona">InternetSetPerSiteCookieDecision</a>
