---
UID: NE:msxml6._XHR_COOKIE_STATE
title: XHR_COOKIE_STATE (msxml6.h)
description: Specifies the state of the cookie.
helpviewer_keywords: ["XHR_COOKIE_STATE","XHR_COOKIE_STATE enumeration [XMLHttpRequest2]","XHR_COOKIE_STATE_ACCEPT","XHR_COOKIE_STATE_DOWNGRADE","XHR_COOKIE_STATE_LEASH","XHR_COOKIE_STATE_PROMPT","XHR_COOKIE_STATE_REJECT","XHR_COOKIE_STATE_UNKNOWN","ixhr2.xhr_cookie_state","msxml6/XHR_COOKIE_STATE","msxml6/XHR_COOKIE_STATE_ACCEPT","msxml6/XHR_COOKIE_STATE_DOWNGRADE","msxml6/XHR_COOKIE_STATE_LEASH","msxml6/XHR_COOKIE_STATE_PROMPT","msxml6/XHR_COOKIE_STATE_REJECT","msxml6/XHR_COOKIE_STATE_UNKNOWN"]
old-location: ixhr2\xhr_cookie_state.htm
tech.root: ixhr2
ms.assetid: 040a5ae8-ec18-44a6-a3e9-376637cc005a
ms.date: 12/05/2018
ms.keywords: XHR_COOKIE_STATE, XHR_COOKIE_STATE enumeration [XMLHttpRequest2], XHR_COOKIE_STATE_ACCEPT, XHR_COOKIE_STATE_DOWNGRADE, XHR_COOKIE_STATE_LEASH, XHR_COOKIE_STATE_PROMPT, XHR_COOKIE_STATE_REJECT, XHR_COOKIE_STATE_UNKNOWN, ixhr2.xhr_cookie_state, msxml6/XHR_COOKIE_STATE, msxml6/XHR_COOKIE_STATE_ACCEPT, msxml6/XHR_COOKIE_STATE_DOWNGRADE, msxml6/XHR_COOKIE_STATE_LEASH, msxml6/XHR_COOKIE_STATE_PROMPT, msxml6/XHR_COOKIE_STATE_REJECT, msxml6/XHR_COOKIE_STATE_UNKNOWN
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: XHR_COOKIE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XHR_COOKIE_STATE
 - msxml6/_XHR_COOKIE_STATE
 - XHR_COOKIE_STATE
 - msxml6/XHR_COOKIE_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msxml6.h
api_name:
 - XHR_COOKIE_STATE
---

# XHR_COOKIE_STATE enumeration


## -description

Specifies the state of the cookie.

## -enum-fields

### -field XHR_COOKIE_STATE_UNKNOWN:0

The state of the cookie is unknown.

### -field XHR_COOKIE_STATE_ACCEPT:0x1

The cookie has been accepted by the client.

### -field XHR_COOKIE_STATE_PROMPT:0x2

The user is being prompted to accept the cookie form the server.

### -field XHR_COOKIE_STATE_LEASH:0x3

### -field XHR_COOKIE_STATE_DOWNGRADE:0x4

### -field XHR_COOKIE_STATE_REJECT:0x5

The cookie has been rejected.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setcookie">SetCookie</a>



<a href="/windows/desktop/api/msxml6/ns-msxml6-xhr_cookie">XHR_COOKIE</a>
