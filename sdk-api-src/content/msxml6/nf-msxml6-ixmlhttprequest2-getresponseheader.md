---
UID: NF:msxml6.IXMLHTTPRequest2.GetResponseHeader
title: IXMLHTTPRequest2::GetResponseHeader (msxml6.h)
description: Retrieves the value of an HTTP header from the response headers.
helpviewer_keywords: ["GetResponseHeader","GetResponseHeader method [XMLHttpRequest2]","GetResponseHeader method [XMLHttpRequest2]","IXMLHTTPRequest2 interface","IXMLHTTPRequest2 interface [XMLHttpRequest2]","GetResponseHeader method","IXMLHTTPRequest2.GetResponseHeader","IXMLHTTPRequest2::GetResponseHeader","ixhr2.ixmlhttprequest2_getresponseheader","msxml6/IXMLHTTPRequest2::GetResponseHeader"]
old-location: ixhr2\ixmlhttprequest2_getresponseheader.htm
tech.root: ixhr2
ms.assetid: 5D68DAAA-D359-4FDF-8250-14A8D732FFFA
ms.date: 12/05/2018
ms.keywords: GetResponseHeader, GetResponseHeader method [XMLHttpRequest2], GetResponseHeader method [XMLHttpRequest2],IXMLHTTPRequest2 interface, IXMLHTTPRequest2 interface [XMLHttpRequest2],GetResponseHeader method, IXMLHTTPRequest2.GetResponseHeader, IXMLHTTPRequest2::GetResponseHeader, ixhr2.ixmlhttprequest2_getresponseheader, msxml6/IXMLHTTPRequest2::GetResponseHeader
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
 - IXMLHTTPRequest2::GetResponseHeader
 - msxml6/IXMLHTTPRequest2::GetResponseHeader
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
 - IXMLHTTPRequest2.GetResponseHeader
---

# IXMLHTTPRequest2::GetResponseHeader


## -description

Retrieves the value of an HTTP header from the response headers.

## -parameters

### -param pwszHeader [in]

A case-insensitive header name.

### -param ppwszValue [out, optional]

The resulting header information. You should free the memory for this parameter by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

Returns <b>S_OK</b> on success.

## -remarks

The results of this method are valid only after <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onheadersavailable">OnHeadersAvailable</a> callback method has been called.


#### Examples


```cpp
HRESULT hr = S_OK;
WCHAR *pwszHeaderValue = NULL;
IXMLHTTPRequest2 *pIXMLHTTPRequest2 = NULL;

// Create XMLHTTPRequest2 object and initialize pIXMLHTTP2Request.
hr = pIXMLHTTPRequest2->GetResponseHeader(L"Server", &pwszHeaderValue);
if(SUCCEEDED(hr))
{
   MessageBox(NULL, pwszHeaderValue, L"Response Header-Server", MB_OK);   
}   

if (pwszHeaderValue != NULL)
{
   CoTaskMemFree(pwszHeaderValue);
   pwszHeaderValue = NULL;
}

// Release pIXMLHTTPRequest2 when finished with it.

```

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-getallresponseheaders">GetAllResponseHeaders</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onheadersavailable">OnHeadersAvailable</a>