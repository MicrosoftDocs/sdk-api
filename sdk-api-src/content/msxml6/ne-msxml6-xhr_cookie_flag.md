---
UID: NE:msxml6._XHR_COOKIE_FLAG
title: XHR_COOKIE_FLAG (msxml6.h)
description: Defines a set of flags that you can assign to a cookie in the HTTP cookie jar by calling the SetCookie method or query from the HTTP cookie jar by calling the GetCookie method.
helpviewer_keywords: ["XHR_COOKIE_APPLY_P3P","XHR_COOKIE_EVALUATE_P3P","XHR_COOKIE_FLAG","XHR_COOKIE_FLAG enumeration [XMLHttpRequest2]","XHR_COOKIE_HTTPONLY","XHR_COOKIE_IE6","XHR_COOKIE_IS_LEGACY","XHR_COOKIE_IS_RESTRICTED","XHR_COOKIE_IS_SECURE","XHR_COOKIE_IS_SESSION","XHR_COOKIE_NON_SCRIPT","XHR_COOKIE_P3P_ENABLED","XHR_COOKIE_PROMPT_REQUIRED","XHR_COOKIE_THIRD_PARTY","ixhr2.xhr_cookie_flag","msxml6/XHR_COOKIE_APPLY_P3P","msxml6/XHR_COOKIE_EVALUATE_P3P","msxml6/XHR_COOKIE_FLAG","msxml6/XHR_COOKIE_HTTPONLY","msxml6/XHR_COOKIE_IE6","msxml6/XHR_COOKIE_IS_LEGACY","msxml6/XHR_COOKIE_IS_RESTRICTED","msxml6/XHR_COOKIE_IS_SECURE","msxml6/XHR_COOKIE_IS_SESSION","msxml6/XHR_COOKIE_NON_SCRIPT","msxml6/XHR_COOKIE_P3P_ENABLED","msxml6/XHR_COOKIE_PROMPT_REQUIRED","msxml6/XHR_COOKIE_THIRD_PARTY"]
old-location: ixhr2\xhr_cookie_flag.htm
tech.root: ixhr2
ms.assetid: 185a75cb-3901-4850-a987-803da50e14fd
ms.date: 12/05/2018
ms.keywords: XHR_COOKIE_APPLY_P3P, XHR_COOKIE_EVALUATE_P3P, XHR_COOKIE_FLAG, XHR_COOKIE_FLAG enumeration [XMLHttpRequest2], XHR_COOKIE_HTTPONLY, XHR_COOKIE_IE6, XHR_COOKIE_IS_LEGACY, XHR_COOKIE_IS_RESTRICTED, XHR_COOKIE_IS_SECURE, XHR_COOKIE_IS_SESSION, XHR_COOKIE_NON_SCRIPT, XHR_COOKIE_P3P_ENABLED, XHR_COOKIE_PROMPT_REQUIRED, XHR_COOKIE_THIRD_PARTY, ixhr2.xhr_cookie_flag, msxml6/XHR_COOKIE_APPLY_P3P, msxml6/XHR_COOKIE_EVALUATE_P3P, msxml6/XHR_COOKIE_FLAG, msxml6/XHR_COOKIE_HTTPONLY, msxml6/XHR_COOKIE_IE6, msxml6/XHR_COOKIE_IS_LEGACY, msxml6/XHR_COOKIE_IS_RESTRICTED, msxml6/XHR_COOKIE_IS_SECURE, msxml6/XHR_COOKIE_IS_SESSION, msxml6/XHR_COOKIE_NON_SCRIPT, msxml6/XHR_COOKIE_P3P_ENABLED, msxml6/XHR_COOKIE_PROMPT_REQUIRED, msxml6/XHR_COOKIE_THIRD_PARTY
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
req.typenames: XHR_COOKIE_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _XHR_COOKIE_FLAG
 - msxml6/_XHR_COOKIE_FLAG
 - XHR_COOKIE_FLAG
 - msxml6/XHR_COOKIE_FLAG
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
 - XHR_COOKIE_FLAG
---

# XHR_COOKIE_FLAG enumeration


## -description

Defines a set of flags that you can assign to a cookie in the HTTP cookie jar by calling the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setcookie">SetCookie</a> method or query from the HTTP cookie jar by calling the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-getcookie">GetCookie</a> method.

## -enum-fields

### -field XHR_COOKIE_IS_SECURE:0x1

The cookie is secure. 

When this flag is set, the client is only to return the cookie in subsequent requests if those requests use HTTPS.

### -field XHR_COOKIE_IS_SESSION:0x2

The cookie is only usable in the current HTTP session and is not persisted or saved.

### -field XHR_COOKIE_THIRD_PARTY:0x10

The cookie being set is a third-party cookie.

### -field XHR_COOKIE_PROMPT_REQUIRED:0x20

A prompt to the user is required to accept the cookie from the server.

### -field XHR_COOKIE_EVALUATE_P3P:0x40

The cookie has a Platform-for-Privacy-Protection (P3P) header.

### -field XHR_COOKIE_APPLY_P3P:0x80

A cookie with a Platform-for-Privacy-Protection (P3P) header has been applied.

### -field XHR_COOKIE_P3P_ENABLED:0x100

A cookie with a Platform-for-Privacy-Protection (P3P) header has been enabled.

### -field XHR_COOKIE_IS_RESTRICTED:0x200

The cookie being set is associated with an untrusted site.

### -field XHR_COOKIE_IE6:0x400

### -field XHR_COOKIE_IS_LEGACY:0x800

### -field XHR_COOKIE_NON_SCRIPT:0x1000

Does not allow a script or other active content to access this cookie.

### -field XHR_COOKIE_HTTPONLY:0x2000

Enables the retrieval of cookies that are marked as "HTTPOnly". 

Do not use this flag if you expose a scriptable interface, because this has security implications. If you expose a scriptable interface, you can become an attack vector for cross-site scripting attacks. It is imperative that you use this flag only if they can guarantee that you will never permit third-party code to set a cookie using this flag by way of an extensibility mechanism you provide.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-getcookie">GetCookie</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setcookie">SetCookie</a>



<a href="/windows/desktop/api/msxml6/ns-msxml6-xhr_cookie">XHR_COOKIE</a>
