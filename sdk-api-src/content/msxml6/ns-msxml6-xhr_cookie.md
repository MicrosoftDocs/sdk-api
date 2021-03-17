---
UID: NS:msxml6.tagXHR_COOKIE
title: XHR_COOKIE (msxml6.h)
description: Defines a cookie that you can add to the HTTP cookie jar by calling the SetCookie method or retrieve from the HTTP cookie jar by calling the GetCookie method.
helpviewer_keywords: ["PXHR_COOKIE","PXHR_COOKIE structure pointer [XMLHttpRequest2]","XHR_COOKIE","XHR_COOKIE structure [XMLHttpRequest2]","XHR_COOKIE_APPLY_P3P","XHR_COOKIE_EVALUATE_P3P","XHR_COOKIE_HTTPONLY","XHR_COOKIE_IE6","XHR_COOKIE_IS_LEGACY","XHR_COOKIE_IS_RESTRICTED","XHR_COOKIE_IS_SECURE","XHR_COOKIE_IS_SESSION","XHR_COOKIE_NON_SCRIPT","XHR_COOKIE_PROMPT_REQUIRED","XHR_COOKIE_THIRD_PARTY","ixhr2.xhr_cookie","msxml6/PXHR_COOKIE","msxml6/XHR_COOKIE","tagXHR_COOKIE"]
old-location: ixhr2\xhr_cookie.htm
tech.root: ixhr2
ms.assetid: 208829B0-DBCC-4C22-910D-D6826283F8A0
ms.date: 12/05/2018
ms.keywords: PXHR_COOKIE, PXHR_COOKIE structure pointer [XMLHttpRequest2], XHR_COOKIE, XHR_COOKIE structure [XMLHttpRequest2], XHR_COOKIE_APPLY_P3P, XHR_COOKIE_EVALUATE_P3P, XHR_COOKIE_HTTPONLY, XHR_COOKIE_IE6, XHR_COOKIE_IS_LEGACY, XHR_COOKIE_IS_RESTRICTED, XHR_COOKIE_IS_SECURE, XHR_COOKIE_IS_SESSION, XHR_COOKIE_NON_SCRIPT, XHR_COOKIE_PROMPT_REQUIRED, XHR_COOKIE_THIRD_PARTY, ixhr2.xhr_cookie, msxml6/PXHR_COOKIE, msxml6/XHR_COOKIE, tagXHR_COOKIE
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XHR_COOKIE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagXHR_COOKIE
 - msxml6/tagXHR_COOKIE
 - XHR_COOKIE
 - msxml6/XHR_COOKIE
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
 - XHR_COOKIE
---

# XHR_COOKIE structure


## -description

Defines a cookie that you can add to the HTTP cookie jar by calling the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setcookie">SetCookie</a> method or retrieve from the HTTP cookie jar by calling the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-getcookie">GetCookie</a> method.

## -struct-fields

### -field pwszUrl

A null-terminated string that specifies the URL in the cookie.

### -field pwszName

A null-terminated string that specifies the name in the cookie.

### -field pwszValue

A null-terminated string that specifies the value in the cookie.

### -field pwszP3PPolicy

A null-terminated string that specifies the user policy in the cookie.

### -field ftExpires

A null-terminated string that specifies the date and time at which the cookie expires.

### -field dwFlags

A set of bit flags that specifies properties of the cookie.

This member can be one of the values from the <b>XHR_COOKIE_FLAG</b> enumeration type defined in the <i>Msxml6.h</i>  header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_IS_SECURE"></a><a id="xhr_cookie_is_secure"></a><dl>
<dt><b>XHR_COOKIE_IS_SECURE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_IS_SESSION"></a><a id="xhr_cookie_is_session"></a><dl>
<dt><b>XHR_COOKIE_IS_SESSION</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The cookie is a session cookie and not  a persistent cookie.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_THIRD_PARTY"></a><a id="xhr_cookie_third_party"></a><dl>
<dt><b>XHR_COOKIE_THIRD_PARTY</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
Indicates that the cookie being set is a third-party cookie.


</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_PROMPT_REQUIRED"></a><a id="xhr_cookie_prompt_required"></a><dl>
<dt><b>XHR_COOKIE_PROMPT_REQUIRED</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_EVALUATE_P3P"></a><a id="xhr_cookie_evaluate_p3p"></a><dl>
<dt><b>XHR_COOKIE_EVALUATE_P3P</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>pwszP3PPolicy</b> member points to a Platform-for-Privacy-Protection (P3P) header for the cookie in question.


</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_APPLY_P3P"></a><a id="xhr_cookie_apply_p3p"></a><dl>
<dt><b>XHR_COOKIE_APPLY_P3P</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_APPLY_P3P"></a><a id="xhr_cookie_apply_p3p"></a><dl>
<dt><b>XHR_COOKIE_APPLY_P3P</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_IS_RESTRICTED"></a><a id="xhr_cookie_is_restricted"></a><dl>
<dt><b>XHR_COOKIE_IS_RESTRICTED</b></dt>
<dt>0x200</dt>
</dl>
</td>
<td width="60%">
Indicates that the cookie being set is associated with an untrusted site.
 


</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_IE6"></a><a id="xhr_cookie_ie6"></a><dl>
<dt><b>XHR_COOKIE_IE6</b></dt>
<dt>0x400</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_IS_LEGACY"></a><a id="xhr_cookie_is_legacy"></a><dl>
<dt><b>XHR_COOKIE_IS_LEGACY</b></dt>
<dt>0x800</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_NON_SCRIPT"></a><a id="xhr_cookie_non_script"></a><dl>
<dt><b>XHR_COOKIE_NON_SCRIPT</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_HTTPONLY"></a><a id="xhr_cookie_httponly"></a><dl>
<dt><b>XHR_COOKIE_HTTPONLY</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Enables the retrieval of cookies that are marked as "HTTPOnly". 

Do not use this flag if you expose a scriptable interface, because this has security implications. If you expose a scriptable interface, you can become an attack vector for cross-site scripting attacks. It is imperative that you use this flag only if they can guarantee that you will never permit third-party code to set a cookie using this flag by way of an extensibility mechanism you provide. 



</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2 Interface</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setcookie">SetCookie Method</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty Method</a>