---
UID: NF:certenroll.IX509CertificateRequest.Encode
title: IX509CertificateRequest::Encode
author: windows-sdk-content
description: Signs and encodes a certificate request and creates a key pair if one does not exist.
old-location: security\ix509certificaterequest_encode_method.htm
tech.root: SecCertEnroll
ms.assetid: 098788f4-539f-420b-a4e1-65625dd56ca1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Encode, Encode method [Security], Encode method [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],Encode method, IX509CertificateRequest.Encode, IX509CertificateRequest::Encode, certenroll/IX509CertificateRequest::Encode, security.ix509certificaterequest_encode_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequest.Encode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509CertificateRequest.Encode
: 
---

# IX509CertificateRequest::Encode


## -description


The <b>Encode</b> method signs and encodes a certificate request and creates a key pair if one does not exist. The request is encoded by using <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) as defined by the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) standard. The encoding process creates a byte array.  You can retrieve the byte array by calling the <a href="https://msdn.microsoft.com/1830a569-03a4-4692-adbf-b627bf4370a1">RawData</a> property. 


## -parameters






## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CERTSRV_E_ARCHIVED_KEY_REQUIRED</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/6d17222e-3657-4911-a8e7-d90214284441">ArchivePrivateKey</a> property has been set for a CMC request but a key exchange certificate could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>OLE_E_BLANK</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The object is not initialized.

</td>
</tr>
</table>
 




## -remarks



For a PKCS #10 request, this method:<ul>
<li>Updates the private key or creates the key if necessary.</li>
<li>Populates the public key from the private key.</li>
<li>Updates the extensions, adding any default extensions and taking account of the suppressed OID collection and critical extension OID collection.</li>
<li>Updates the attributes, adding default attributes and taking account of the suppressed OID collection.</li>
<li>Assembles and encodes the unsigned updated request.</li>
<li>Creates and encodes a signature.</li>
<li>Encodes the signature and the unsigned request.</li>
</ul>


For a CMC request, this method:<ul>
<li>Encodes all inner request objects.</li>
<li>Updates the extensions for the outer request object, adding any default extensions and taking account of the suppressed OID collection and critical extension OID collection.</li>
<li>Updates the attributes for the outer request object, adding default attributes and taking account of the suppressed OID collection.</li>
<li>Updates the name-value pair collection.</li>
<li>Encodes the CMC content that consists of the encoded inner request and the updated outer request.</li>
<li>Creates and encodes a signature for each signing certificate.</li>
<li>Creates and encodes a  primary signature.</li>
<li>Assembles the encoded CMC content (including the inner request and the updated outer request) and the encoded signatures.</li>
<li>Encodes the assembled content into a PKCS #7 message.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

