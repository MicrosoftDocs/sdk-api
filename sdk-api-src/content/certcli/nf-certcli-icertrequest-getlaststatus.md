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

# ICertRequest::GetLastStatus


## -description


The <b>GetLastStatus</b> method gets the last return code for this request. This returns the error code information, rather than the disposition of the request.


## -parameters




### -param pStatus [out]

A pointer to the request's status code.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

Upon successful completion of this function, *<i>pStatus</i> is set to the result code of the latest call to <a href="https://msdn.microsoft.com/22ae8d39-3f16-4f7d-94a0-aa68b03aaa0b">ICertRequest3::Submit</a>, <a href="https://msdn.microsoft.com/07a9ac57-f90e-4c5c-b563-8aebbcf8f42e">ICertRequest3::RetrievePending</a>, or <a href="https://msdn.microsoft.com/711fdcec-0a07-4559-a577-1eb73053dd38">ICertRequest3::GetCACertificate</a>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the result code of the latest call to <a href="https://msdn.microsoft.com/22ae8d39-3f16-4f7d-94a0-aa68b03aaa0b">CCertRequest3.Submit</a>, <a href="https://msdn.microsoft.com/07a9ac57-f90e-4c5c-b563-8aebbcf8f42e">CCertRequest3.RetrievePending</a> or <a href="https://msdn.microsoft.com/711fdcec-0a07-4559-a577-1eb73053dd38">CCertRequest3.GetCACertificate</a>.




## -remarks



The value retrieved by <b>GetLastStatus</b> depends on the most recent call to 
<a href="https://msdn.microsoft.com/22ae8d39-3f16-4f7d-94a0-aa68b03aaa0b">ICertRequest3::Submit</a>, 
<a href="https://msdn.microsoft.com/07a9ac57-f90e-4c5c-b563-8aebbcf8f42e">ICertRequest3::RetrievePending</a>, or 
<a href="https://msdn.microsoft.com/711fdcec-0a07-4559-a577-1eb73053dd38">ICertRequest3::GetCACertificate</a>. If a call to one of these methods fails on the server, call <b>GetLastStatus</b> to retrieve the error number. Some server failures (such as denied requests) return S_OK and a disposition other than CR_DISP_ISSUED from the method call, and you can use <b>GetLastStatus</b> to retrieve the specific cause of failure. If a call to one of these methods succeeds, then a subsequent call to <b>GetLastStatus</b> returns S_OK (which is zero).

Additionally, the request disposition is stored in the Certificate Services database, and can be viewed by means of the Certification Authority MMC snap-in (choose the Request Disposition column).


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT    hrServer, hr;
// pCertRequest is previously instantiated
// ICertRequest object pointer.
hr = pCertRequest-&gt;GetLastStatus((LONG *) &amp;hrServer);
if (FAILED(hr))
{
    printf("Failed GetLastStatus [%x]\n", hr);
    goto error;
}
else
{
    // Use the HRESULT value as needed...
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">CCertRequest</a>



<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">ICertRequest</a>



<a href="https://msdn.microsoft.com/8587a682-27a5-4f26-b4bb-7088e4e5d8d3">ICertRequest2</a>



<a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a>
 

 

