---
UID: NF:certenroll.IX509CertificateRequest.get_AlternateSignatureAlgorithm
title: IX509CertificateRequest::get_AlternateSignatureAlgorithm (certenroll.h)
description: Specifies and retrieves a Boolean value that indicates whether the signature algorithm object identifier (OID) for a PKCS (Get)
helpviewer_keywords: ["AlternateSignatureAlgorithm property [Security]","AlternateSignatureAlgorithm property [Security]","IX509CertificateRequest interface","IX509CertificateRequest interface [Security]","AlternateSignatureAlgorithm property","IX509CertificateRequest.AlternateSignatureAlgorithm","IX509CertificateRequest.get_AlternateSignatureAlgorithm","IX509CertificateRequest::AlternateSignatureAlgorithm","IX509CertificateRequest::get_AlternateSignatureAlgorithm","IX509CertificateRequest::put_AlternateSignatureAlgorithm","certenroll/IX509CertificateRequest::AlternateSignatureAlgorithm","certenroll/IX509CertificateRequest::get_AlternateSignatureAlgorithm","certenroll/IX509CertificateRequest::put_AlternateSignatureAlgorithm","get_AlternateSignatureAlgorithm","security.ix509certificaterequest_alternatesignaturealgorithm_property"]
old-location: security\ix509certificaterequest_alternatesignaturealgorithm_property.htm
tech.root: security
ms.assetid: 57a87aab-1e53-4b0b-a7b9-2fe89083819b
ms.date: 12/05/2018
ms.keywords: AlternateSignatureAlgorithm property [Security], AlternateSignatureAlgorithm property [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],AlternateSignatureAlgorithm property, IX509CertificateRequest.AlternateSignatureAlgorithm, IX509CertificateRequest.get_AlternateSignatureAlgorithm, IX509CertificateRequest::AlternateSignatureAlgorithm, IX509CertificateRequest::get_AlternateSignatureAlgorithm, IX509CertificateRequest::put_AlternateSignatureAlgorithm, certenroll/IX509CertificateRequest::AlternateSignatureAlgorithm, certenroll/IX509CertificateRequest::get_AlternateSignatureAlgorithm, certenroll/IX509CertificateRequest::put_AlternateSignatureAlgorithm, get_AlternateSignatureAlgorithm, security.ix509certificaterequest_alternatesignaturealgorithm_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509CertificateRequest::get_AlternateSignatureAlgorithm
 - certenroll/IX509CertificateRequest::get_AlternateSignatureAlgorithm
dev_langs:
 - c++
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
---

# IX509CertificateRequest::get_AlternateSignatureAlgorithm


## -description

The <b>AlternateSignatureAlgorithm</b> property specifies and retrieves a Boolean value that indicates whether the signature algorithm <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) for a PKCS #10 request or certificate signature is discrete or combined. A PKCS #10 object can be a stand-alone request or it can be contained in a CMC or PKCS #7 request object.

This property is read/write.

## -parameters

## -remarks

Discrete algorithms are represented by separate <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) for the hashing algorithm and the signing algorithm. Examples include the following values.<table>
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

You must initialize the request object before calling this property. You can call this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a>
