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

# IXMLHTTPRequest2::GetAllResponseHeaders


## -description


Retrieves the values of all the HTTP response headers.


## -parameters




### -param ppwszHeaders [out]

The returned header information. Free the memory used for this parameter using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> method.


## -returns



Returns <b>S_OK</b> on success.




## -remarks



Each header name/value pair is separated by a combination carriage return-line feed.

The returned response header information is only valid after the <a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a> callback method has been called.


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

// Create IXMLHTTPRequest2 object and initialize pIXMLHTTPRequest2.
hr = pIXMLHTTPRequest2-&gt;GetAllResponseHeaders(&amp;pwszHeaderValue);
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>



<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>



<a href="https://msdn.microsoft.com/EB6580C5-B200-4281-BF1F-FA5C3220689E">OnHeadersAvailable</a>
 

 

