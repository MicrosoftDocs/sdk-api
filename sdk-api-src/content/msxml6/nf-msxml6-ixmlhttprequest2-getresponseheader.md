---
UID: NF:msxml6.IXMLHTTPRequest2.GetResponseHeader
title: IXMLHTTPRequest2::GetResponseHeader
author: windows-sdk-content
description: Retrieves the value of an HTTP header from the response headers.
old-location: ixhr2\ixmlhttprequest2_getresponseheader.htm
tech.root: ixhr2
ms.assetid: 5D68DAAA-D359-4FDF-8250-14A8D732FFFA
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetResponseHeader, GetResponseHeader method [XMLHttpRequest2], GetResponseHeader method [XMLHttpRequest2],IXMLHTTPRequest2 interface, IXMLHTTPRequest2 interface [XMLHttpRequest2],GetResponseHeader method, IXMLHTTPRequest2.GetResponseHeader, IXMLHTTPRequest2::GetResponseHeader, ixhr2.ixmlhttprequest2_getresponseheader, msxml6/IXMLHTTPRequest2::GetResponseHeader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IXMLHTTPRequest2.GetResponseHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXMLHTTPRequest2::GetResponseHeader


## -description


Retrieves the value of an HTTP header from the response headers.


## -parameters




### -param pwszHeader [in]

A case-insensitive header name.


### -param ppwszValue [out, optional]

The resulting header information. You should free the memory for this parameter by calling the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.


## -returns



Returns <b>S_OK</b> on success.




## -remarks



The results of this method are valid only after <a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a> callback method has been called.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr = S_OK;
WCHAR *pwszHeaderValue = NULL;
IXMLHTTPRequest2 *pIXMLHTTPRequest2 = NULL;

// Create XMLHTTPRequest2 object and initialize pIXMLHTTP2Request.
hr = pIXMLHTTPRequest2-&gt;GetResponseHeader(L"Server", &amp;pwszHeaderValue);
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>



<a href="https://msdn.microsoft.com/6452812B-0E0F-4140-8E3C-25592A9C6C48">GetAllResponseHeaders</a>



<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>



<a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a>
 

 

