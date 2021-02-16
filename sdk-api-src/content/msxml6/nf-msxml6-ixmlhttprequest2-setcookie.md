---
UID: NF:msxml6.IXMLHTTPRequest2.SetCookie
title: IXMLHTTPRequest2::SetCookie (msxml6.h)
description: Sets a cookie associated with the specified URL in the HTTP cookie jar.
helpviewer_keywords: ["IXMLHTTPRequest2 interface [XMLHttpRequest2]","SetCookie method","IXMLHTTPRequest2.SetCookie","IXMLHTTPRequest2::SetCookie","SetCookie","SetCookie method [XMLHttpRequest2]","SetCookie method [XMLHttpRequest2]","IXMLHTTPRequest2 interface","XHR_COOKIE_STATE_ACCEPT","XHR_COOKIE_STATE_DOWNGRADE","XHR_COOKIE_STATE_LEASH","XHR_COOKIE_STATE_PROMPT","XHR_COOKIE_STATE_REJECT","XHR_COOKIE_STATE_UNKNOWN","ixhr2.ixmlhttprequest2_setcookie","msxml6/IXMLHTTPRequest2::SetCookie"]
old-location: ixhr2\ixmlhttprequest2_setcookie.htm
tech.root: ixhr2
ms.assetid: E150B7CA-A881-4CD5-896F-7E3B6770E105
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2 interface [XMLHttpRequest2],SetCookie method, IXMLHTTPRequest2.SetCookie, IXMLHTTPRequest2::SetCookie, SetCookie, SetCookie method [XMLHttpRequest2], SetCookie method [XMLHttpRequest2],IXMLHTTPRequest2 interface, XHR_COOKIE_STATE_ACCEPT, XHR_COOKIE_STATE_DOWNGRADE, XHR_COOKIE_STATE_LEASH, XHR_COOKIE_STATE_PROMPT, XHR_COOKIE_STATE_REJECT, XHR_COOKIE_STATE_UNKNOWN, ixhr2.ixmlhttprequest2_setcookie, msxml6/IXMLHTTPRequest2::SetCookie
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXMLHTTPRequest2::SetCookie
 - msxml6/IXMLHTTPRequest2::SetCookie
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest2.SetCookie
---

# IXMLHTTPRequest2::SetCookie


## -description

Sets a cookie associated with the specified URL in the HTTP cookie jar.

## -parameters

### -param pCookie

A pointer to an <a href="/windows/desktop/api/msxml6/ns-msxml6-xhr_cookie">XHR_COOKIE</a> structure that specifies the cookie and properties of the cookie to be associated with  the specified URL.

### -param pdwCookieState

A pointer to a value that indicates the cookie state if the call completes successfully. 

This parameter can be one of the values from the <a href="/windows/desktop/api/msxml6/ne-msxml6-xhr_cookie_state">XHR_COOKIE_STATE</a> enumeration type defined in the <i>Msxml6.h</i>  header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_UNKNOWN"></a><a id="xhr_cookie_state_unknown"></a><dl>
<dt><b>XHR_COOKIE_STATE_UNKNOWN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Reserved.



</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_ACCEPT"></a><a id="xhr_cookie_state_accept"></a><dl>
<dt><b>XHR_COOKIE_STATE_ACCEPT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The cookie was accepted.



</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_PROMPT"></a><a id="xhr_cookie_state_prompt"></a><dl>
<dt><b>XHR_COOKIE_STATE_PROMPT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The user is prompted to accept or refuse the cookie.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_LEASH"></a><a id="xhr_cookie_state_leash"></a><dl>
<dt><b>XHR_COOKIE_STATE_LEASH</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The cookie is accepted only in the first-party context.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_DOWNGRADE"></a><a id="xhr_cookie_state_downgrade"></a><dl>
<dt><b>XHR_COOKIE_STATE_DOWNGRADE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The cookie was accepted and became session cookie.

</td>
</tr>
<tr>
<td width="40%"><a id="XHR_COOKIE_STATE_REJECT"></a><a id="xhr_cookie_state_reject"></a><dl>
<dt><b>XHR_COOKIE_STATE_REJECT</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The cookie was rejected.



</td>
</tr>
</table>

## -returns

Returns <b>S_OK</b> on success.

## -remarks

The <b>SetCookie</b> method has different behavior for Windows Store apps and Windows desktop applications. 

When used in a Windows Store app, the <b>SetCookie</b> method  by default sets the cookie as a persistent cookie in the Windows Store app. When the <b>dwFlags</b> member of the <a href="/windows/desktop/api/msxml6/ns-msxml6-xhr_cookie">XHR_COOKIE</a> has the <b>XHR_COOKIE_IS_SESSION</b> flag set, then the cookie is set only for the current session of the app.

When used in a Windows desktop application, the <b>SetCookie</b> method  by default sets a persistent cookie that  is system wide and shared by all Windows desktop applications.   When the <b>dwFlags</b> member of the <a href="/windows/desktop/api/msxml6/ns-msxml6-xhr_cookie">XHR_COOKIE</a> has the <b>XHR_COOKIE_IS_SESSION</b> flag set, then the cookie is set only for the current session of the Windows desktop application.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-getcookie">GetCookie Method</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>



<a href="/windows/desktop/api/msxml6/ns-msxml6-xhr_cookie">XHR_COOKIE Structure</a>



<a href="/windows/desktop/api/msxml6/ne-msxml6-xhr_cookie_state">XHR_COOKIE_STATE</a>