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

# ICertServerPolicy::GetRequestAttribute


## -description


The <b>GetRequestAttribute</b> method returns a named <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> from a request.


## -parameters




### -param strAttributeName [in]

The name of the attribute to retrieve.


### -param pstrAttributeValue [out]

A pointer to a <b>BSTR</b> value that will contain the attribute value.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK and *<i>pstrAttributeValue</i> is set to the <b>BSTR</b> that contains the attribute value.

To use this method, create a variable of type <b>BSTR</b>, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrAttributeValue</i>.

When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a string that represents the attribute value.




## -remarks



You must call 
<a href="https://msdn.microsoft.com/ba45cda8-49a5-4bd6-af68-90b4b56aff7d">ICertServerPolicy::SetContext</a> prior to using this method.

The following request attributes are unique to KEYGEN style requests.

<table>
<tr>
<th>Property name</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>Challenge</td>
<td><b>String</b></td>
<td>Challenge string that accompanies the request.</td>
</tr>
<tr>
<td>ExpectedChallenge</td>
<td><b>String</b></td>
<td>If the challenge string is incorrect, then the server will set the value of this request attribute to the expected challenge so that failure can be diagnosed.</td>
</tr>
</table>
 


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR     bstrAttribValue = NULL;
HRESULT  hr;

// Get the request attribute.
// bstrAttribName is BSTR assigned by EnumerateAttributes.
// pCertServerPolicy has been used to call SetContext previously.
hr = pCertServerPolicy-&gt;GetRequestAttribute(bstrAttribName,
                                            &amp;bstrAttribValue);

if (FAILED(hr))
{
    printf("Failed GetRequestAttribute [%x]\n", hr);
    goto error;
}
else
{

    // Successful call. Use the bstrAttribValue as needed.
    // ...
}

// Done processing. Free BSTR.
if (NULL != bstrAttribValue)
    SysFreeString(bstrAttribValue);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7d16161e-9827-46a0-9989-30ebca792bb1">ICertServerPolicy</a>



<a href="https://msdn.microsoft.com/ba45cda8-49a5-4bd6-af68-90b4b56aff7d">ICertServerPolicy::SetContext</a>
 

 

