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

# ICertAdmin::GetRevocationReason


## -description


The <b>GetRevocationReason</b> method  returns  the reason a certificate was revoked. This method was first defined in the <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a> interface.

Before you call this method, you must call the 
<a href="https://msdn.microsoft.com/cd133c57-a62e-4083-b4fd-7eaf0c9e7606">IsValidCertificate</a> method. For more information, see Remarks.


## -parameters




### -param pReason [out]

A pointer to a variable that will receive the revocation reason.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and  the <i>pReason</i> parameter is set to one of the values listed in the following table.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a value that specifies the reason the certificate was revoked. The value can be one of the following revocation reason codes (defined in Wincrypt.h).

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_UNSPECIFIED</b></dt>
</dl>
</td>
<td width="60%">
No reason was specified for revocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_KEY_COMPROMISE</b></dt>
</dl>
</td>
<td width="60%">
It is known or suspected that the subject's private key or other aspects of the subject validated in the certificate are compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_CA_COMPROMISE</b></dt>
</dl>
</td>
<td width="60%">
It is known or suspected that the CA's private key or other aspects of the CA validated in the certificate are compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_AFFILIATION_CHANGED</b></dt>
</dl>
</td>
<td width="60%">
The subject's name or other information in the certificate has been modified but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_SUPERSEDED</b></dt>
</dl>
</td>
<td width="60%">
The certificate has been superseded, but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_CESSATION_OF_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The certificate is no longer needed for the purpose for which it was issued, but there is no cause to suspect that the private key has been compromised.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRL_REASON_CERTIFICATE_HOLD</b></dt>
</dl>
</td>
<td width="60%">
The certificate has been placed on hold.

</td>
</tr>
</table>
 




## -remarks



Before you call <b>GetRevocationReason</b>, call the 
<a href="https://msdn.microsoft.com/cd133c57-a62e-4083-b4fd-7eaf0c9e7606">IsValidCertificate</a> method to retrieve the disposition of the certificate. To call <b>GetRevocationReason</b>, you must receive a certificate disposition CA_DISP_REVOKED from this earlier call, indicating that the certificate has been revoked. The call to <b>IsValidCertificate</b> establishes the identity of the certificate whose revocation reason you want to retrieve.

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// The value for nDisp was set by 
// a call to ICertAdmin2::IsValidCertificate.
if (CA_DISP_REVOKED == nDisp)
{
    // Variable to contain revocation reason.
    long       nReason;

    // Retrieve the revocation reason.
    hr = pCertAdmin-&gt;GetRevocationReason(&amp;nReason);
    if (FAILED(hr))
    {
        printf("Failed GetRevocationReason [%x]\n", hr);
        goto error;
    }
    else
        printf("Revocation reason = %d\n", nReason );
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">CCertAdmin</a>



<a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a>



<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin2</a>



<a href="https://msdn.microsoft.com/cd133c57-a62e-4083-b4fd-7eaf0c9e7606">IsValidCertificate</a>
 

 

