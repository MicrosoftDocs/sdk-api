---
UID: NF:certenroll.IX509CertificateRequest.get_AlternateSignatureAlgorithm
title: IX509CertificateRequest::get_AlternateSignatureAlgorithm
author: windows-sdk-content
description: Specifies and retrieves a Boolean value that indicates whether the signature algorithm object identifier (OID) for a PKCS #10 request or certificate signature is discrete or combined.
old-location: security\ix509certificaterequest_alternatesignaturealgorithm_property.htm
tech.root: SecCertEnroll
ms.assetid: 57a87aab-1e53-4b0b-a7b9-2fe89083819b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AlternateSignatureAlgorithm property [Security], AlternateSignatureAlgorithm property [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],AlternateSignatureAlgorithm property, IX509CertificateRequest.AlternateSignatureAlgorithm, IX509CertificateRequest.get_AlternateSignatureAlgorithm, IX509CertificateRequest::AlternateSignatureAlgorithm, IX509CertificateRequest::get_AlternateSignatureAlgorithm, IX509CertificateRequest::put_AlternateSignatureAlgorithm, certenroll/IX509CertificateRequest::AlternateSignatureAlgorithm, certenroll/IX509CertificateRequest::get_AlternateSignatureAlgorithm, certenroll/IX509CertificateRequest::put_AlternateSignatureAlgorithm, get_AlternateSignatureAlgorithm, security.ix509certificaterequest_alternatesignaturealgorithm_property
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
 - IX509CertificateRequest.AlternateSignatureAlgorithm
 - IX509CertificateRequest.get_AlternateSignatureAlgorithm
 - IX509CertificateRequest.put_AlternateSignatureAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest::get_AlternateSignatureAlgorithm


## -description


The <b>AlternateSignatureAlgorithm</b> property specifies and retrieves a Boolean value that indicates whether the signature algorithm <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) for a PKCS #10 request or certificate signature is discrete or combined. A PKCS #10 object can be a stand-alone request or it can be contained in a CMC or PKCS #7 request object.

This property is read/write.


## -parameters


## -remarks



Discrete algorithms are represented by separate <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifiers</a> (OIDs) for the hashing algorithm and the signing algorithm. Examples include the following values.<table>
<tr>
<th>Discrete algorithm OID</th>
<th>Description</th>
</tr>
<tr>
<td>
XCN_OID_NIST_sha256

(2.16.840.1.101.3.4.2.1)

</td>
<td>
National Institute of Standards and Technologies (NIST) 256-bit SHA hashing algorithm.

</td>
</tr>
<tr>
<td>
XCN_OID_OIWSEC_rsaSign

(1.3.14.3.2.11)

</td>
<td>
NIST OSE Implementer Workshop Security (OIWSEC) RSA signing algorithm.

</td>
</tr>
</table>
 



Combined algorithms are represented by a single OID that identifies both the hashing and the signing algorithm. Examples include the following values.<table>
<tr>
<th>Combined algorithm OID</th>
<th>Description</th>
</tr>
<tr>
<td>
XCN_OID_RSA_MD2RSA

(1.2.840.113549.1.1.2)

</td>
<td>
MD2 hashing algorithm combined with the RSA encryption algorithm from RSA Laboratories.

</td>
</tr>
<tr>
<td>
XCN_OID_OIWSEC_md5RSA

(1.3.14.3.2.3)

</td>
<td>
OIWSEC MD5 hashing algorithm combined with the RSA encryption algorithm.

</td>
</tr>
</table>
 



If the certificate request contains nested requests and you set the <b>AlternateSignatureAlgorithm</b> property on the top level request, it is automatically propagated to all of the inner requests. You can, however, set the property manually on each of the inner objects.

For a PKCS #7 or a CMC request, this property retrieves a Boolean value for the primary signature on the inner PKCS #10 request. On input, all signer certificates are updated with the specified property value.

For a PKCS #10 request or certificate signature using the RSA public key algorithm, a property value of False (which indicates a combined OID) implies a version 1.5 signature and True (discrete OID) implies a version 2.1 signature.

You must initialize the request object before calling this property. You can call this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 

