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

# ICertServerPolicy::EnumerateExtensionsClose


## -description


The <b>EnumerateExtensionsClose</b> method frees the resources connected with extension enumeration.


## -parameters






## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



All policy modules should call the <b>EnumerateExtensionsClose</b> method after calling the <a href="https://msdn.microsoft.com/e7ad32a5-d7df-407f-8efe-c9931610c2d2">EnumerateExtensionsSetup</a> and 
<a href="https://msdn.microsoft.com/565ff4d5-0d22-466d-8458-f98b992a1868">ICertServerPolicy::EnumerateExtensions</a> methods.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Close the enumeration.
// hr is defined as an HRESULT.
hr = pCertServerPolicy-&gt;EnumerateExtensionsClose();
if (FAILED(hr))
{
    printf("Failed EnumerateExtensionsClose [%x]\n", hr);
    goto error;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2a0c4919-b3a0-4027-85bd-970f6bc0cdeb">ICertServerExit::EnumerateExtensionsSetup</a>



<a href="https://msdn.microsoft.com/7d16161e-9827-46a0-9989-30ebca792bb1">ICertServerPolicy</a>



<a href="https://msdn.microsoft.com/565ff4d5-0d22-466d-8458-f98b992a1868">ICertServerPolicy::EnumerateExtensions</a>
 

 

