---
UID: NF:certcli.ICertRequest.GetLastStatus
title: ICertRequest::GetLastStatus
author: windows-sdk-content
description: Gets the last return code for this request. This returns the error code information, rather than the disposition of the request.
old-location: security\icertrequest2_getlaststatus.htm
tech.root: seccrypto
ms.assetid: ebe5cfa7-6bfd-4454-9272-64e3b1bf0ae2
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: CCertRequest object [Security],GetLastStatus method, GetLastStatus, GetLastStatus method [Security], GetLastStatus method [Security],CCertRequest object, GetLastStatus method [Security],ICertRequest interface, GetLastStatus method [Security],ICertRequest2 interface, GetLastStatus method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetLastStatus method, ICertRequest.GetLastStatus, ICertRequest2 interface [Security],GetLastStatus method, ICertRequest2::GetLastStatus, ICertRequest3 interface [Security],GetLastStatus method, ICertRequest3::GetLastStatus, ICertRequest::GetLastStatus, certcli/ICertRequest2::GetLastStatus, certcli/ICertRequest3::GetLastStatus, certcli/ICertRequest::GetLastStatus, security.icertrequest2_getlaststatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certcli.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest3.GetLastStatus
 - ICertRequest2.GetLastStatus
 - ICertRequest.GetLastStatus
 - CCertRequest.GetLastStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Upon successful completion of this function, *<i>pStatus</i> is set to the result code of the latest call to <a href="https://msdn.microsoft.com/en-us/library/Aa385054(v=VS.85).aspx">ICertRequest3::Submit</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa385053(v=VS.85).aspx">ICertRequest3::RetrievePending</a>, or <a href="https://msdn.microsoft.com/en-us/library/Aa385042(v=VS.85).aspx">ICertRequest3::GetCACertificate</a>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the result code of the latest call to <a href="https://msdn.microsoft.com/en-us/library/Aa385054(v=VS.85).aspx">CCertRequest3.Submit</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa385053(v=VS.85).aspx">CCertRequest3.RetrievePending</a> or <a href="https://msdn.microsoft.com/en-us/library/Aa385042(v=VS.85).aspx">CCertRequest3.GetCACertificate</a>.




## -remarks



The value retrieved by <b>GetLastStatus</b> depends on the most recent call to 
<a href="https://msdn.microsoft.com/en-us/library/Aa385054(v=VS.85).aspx">ICertRequest3::Submit</a>, 
<a href="https://msdn.microsoft.com/en-us/library/Aa385053(v=VS.85).aspx">ICertRequest3::RetrievePending</a>, or 
<a href="https://msdn.microsoft.com/en-us/library/Aa385042(v=VS.85).aspx">ICertRequest3::GetCACertificate</a>. If a call to one of these methods fails on the server, call <b>GetLastStatus</b> to retrieve the error number. Some server failures (such as denied requests) return S_OK and a disposition other than CR_DISP_ISSUED from the method call, and you can use <b>GetLastStatus</b> to retrieve the specific cause of failure. If a call to one of these methods succeeds, then a subsequent call to <b>GetLastStatus</b> returns S_OK (which is zero).

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




<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">CCertRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385040(v=VS.85).aspx">ICertRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385041(v=VS.85).aspx">ICertRequest2</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee373776(v=VS.85).aspx">ICertRequest3</a>
 

 

