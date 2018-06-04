---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

