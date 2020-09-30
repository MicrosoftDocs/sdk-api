---
UID: NF:msxml6.IXMLHTTPRequest2.GetCookie
title: IXMLHTTPRequest2::GetCookie (msxml6.h)
description: Gets a cookie associated with the specified URL from the HTTP cookie jar.
helpviewer_keywords: ["GetCookie","GetCookie method [XMLHttpRequest2]","GetCookie method [XMLHttpRequest2]","IXMLHTTPRequest2 interface","IXMLHTTPRequest2 interface [XMLHttpRequest2]","GetCookie method","IXMLHTTPRequest2.GetCookie","IXMLHTTPRequest2::GetCookie","ixhr2.ixmlhttprequest2_getcookie","msxml6/IXMLHTTPRequest2::GetCookie"]
old-location: ixhr2\ixmlhttprequest2_getcookie.htm
tech.root: ixhr2
ms.assetid: A2A9C54B-92A2-41EA-A741-797BA219BCDA
ms.date: 12/05/2018
ms.keywords: GetCookie, GetCookie method [XMLHttpRequest2], GetCookie method [XMLHttpRequest2],IXMLHTTPRequest2 interface, IXMLHTTPRequest2 interface [XMLHttpRequest2],GetCookie method, IXMLHTTPRequest2.GetCookie, IXMLHTTPRequest2::GetCookie, ixhr2.ixmlhttprequest2_getcookie, msxml6/IXMLHTTPRequest2::GetCookie
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
 - IXMLHTTPRequest2::GetCookie
 - msxml6/IXMLHTTPRequest2::GetCookie
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
 - IXMLHTTPRequest2.GetCookie
---

# IXMLHTTPRequest2::GetCookie


## -description

Gets a cookie associated with the specified URL from the HTTP cookie jar.

## -parameters

### -param pwszUrl

A null-terminated string that specifies the URL in the cookie.

### -param pwszName

A null-terminated string that specifies the name in the cookie.

### -param dwFlags

A set of bit flags that specifies how this method retrieves the cookies. This parameter can be a set values from the <a href="/windows/desktop/api/msxml6/ne-msxml6-xhr_cookie_flag">XHR_COOKIE_FLAG</a> enumeration type defined in the <i>Msxml6.h</i> header file.

### -param pcCookies

A count of cookies pointed to by the <i>ppCookies</i> if the call is successful.

### -param ppCookies [out]

A pointer to the cookies associated with the specified <i>pwszUrl</i> and <i>pwszName</i>.

## -returns

Returns <b>S_OK</b> on success; <b>E_FAIL</b> indicates an error.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree Function</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setcookie">SetCookie Method</a>



<a href="/windows/desktop/api/msxml6/ns-msxml6-xhr_cookie">XHR_COOKIE Structure</a>



<a href="/windows/desktop/api/msxml6/ne-msxml6-xhr_cookie_flag">XHR_COOKIE_FLAG</a>