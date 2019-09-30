---
UID: NF:msxml6.IXMLHTTPRequest2.GetAllResponseHeaders
title: IXMLHTTPRequest2::GetAllResponseHeaders (msxml6.h)
author: windows-sdk-content
description: Retrieves the values of all the HTTP response headers.
old-location: ixhr2\ixmlhttprequest2_getallresponseheaders.htm
tech.root: ixhr2
ms.assetid: 6452812B-0E0F-4140-8E3C-25592A9C6C48
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAllResponseHeaders, GetAllResponseHeaders method [XMLHttpRequest2], GetAllResponseHeaders method [XMLHttpRequest2],IXMLHTTPRequest2 interface, IXMLHTTPRequest2 interface [XMLHttpRequest2],GetAllResponseHeaders method, IXMLHTTPRequest2.GetAllResponseHeaders, IXMLHTTPRequest2::GetAllResponseHeaders, ixhr2.ixmlhttprequest2_getallresponseheaders, msxml6/IXMLHTTPRequest2::GetAllResponseHeaders
ms.topic: method
f1_keywords: 
 - "msxml6/IXMLHTTPRequest2.GetAllResponseHeaders"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest2.GetAllResponseHeaders
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXMLHTTPRequest2::GetAllResponseHeaders


## -description


Retrieves the values of all the HTTP response headers.


## -parameters




### -param ppwszHeaders [out]

The returned header information. Free the memory used for this parameter using the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> method.


## -returns



Returns <b>S_OK</b> on success.




## -remarks



Each header name/value pair is separated by a combination carriage return-line feed.

The returned response header information is only valid after the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onheadersavailable">OnHeadersAvailable</a> callback method has been called.


#### Examples


```cpp
HRESULT hr = S_OK;
WCHAR *pwszHeaderValue = NULL;
IXMLHTTPRequest2 *pIXMLHTTPRequest2 = NULL;

// Create IXMLHTTPRequest2 object and initialize pIXMLHTTPRequest2.
hr = pIXMLHTTPRequest2->GetAllResponseHeaders(&pwszHeaderValue);
if(SUCCEEDED(hr))
{
  MessageBox(NULL, pwszHeaderValue, L"All Response Headers", MB_OK);
}

if (pwszHeaderValue != NULL)
{
      CoTaskMemFree(pwszHeaderValue);
      pwszHeaderValue = NULL;
}

// Release pIXMLHTTPRequest2 when finished with it.

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2callback-onheadersavailable">OnHeadersAvailable</a>
 

 

