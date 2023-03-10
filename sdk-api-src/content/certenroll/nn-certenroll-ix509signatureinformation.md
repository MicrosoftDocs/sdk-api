---
UID: NN:certenroll.IX509SignatureInformation
title: IX509SignatureInformation (certenroll.h)
description: Represents information used to sign a certificate request.
helpviewer_keywords: ["IX509SignatureInformation","IX509SignatureInformation interface [Security]","IX509SignatureInformation interface [Security]","described","certenroll/IX509SignatureInformation","security.ix509signatureinformation"]
old-location: security\ix509signatureinformation.htm
tech.root: security
ms.assetid: 25774ccb-8e76-443d-89da-177d6e77c019
ms.date: 12/05/2018
ms.keywords: IX509SignatureInformation, IX509SignatureInformation interface [Security], IX509SignatureInformation interface [Security],described, certenroll/IX509SignatureInformation, security.ix509signatureinformation
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
 - IX509SignatureInformation
 - certenroll/IX509SignatureInformation
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
 - IX509SignatureInformation
---

# IX509SignatureInformation interface


## -description

The <b>IX509SignatureInformation</b> interface represents information used to sign a <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. This includes signature, <a href="/windows/desktop/SecGloss/h-gly">hash</a>, and <a href="/windows/desktop/SecGloss/p-gly">public key algorithms</a>, and public key parameters. The signature process consists of digesting the certificate request by using a hash algorithm, encoding the digest and the hash algorithm identifier by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER), and signing (encrypting) the result.

The algorithms used in this process can be either discrete or combined. Discrete algorithms are represented by separate <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) for the hashing algorithm and the signing algorithm. Discrete algorithms are used when signing a PKCS #7 or CMC request. Examples include the following values.<table>
<tr>
<th>Discrete algorithm OID</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_OID_NIST_sha256(2.16.840.1.101.3.4.2.1)

</td>
<td>National Institute of Standards and Technologies (NIST) 256-bit SHA hashing algorithm.</td>
</tr>
<tr>
<td>XCN_OID_OIWSEC_rsaSign(1.3.14.3.2.11)

</td>
<td>NIST OSE Implementer Workshop Security (OIWSEC) RSA signing algorithm.</td>
</tr>
</table>
 



Combined algorithms, which can be used to sign PKCS #10 requests, are represented by a single OID that identifies both the hashing and the signing algorithm. Examples include the following values.<table>
<tr>
<th>Combined algorithm OID</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_OID_RSA_MD2RSA(1.2.840.113549.1.1.2)

</td>
<td>MD2 hashing algorithm combined with the RSA encryption algorithm from RSA Laboratories.</td>
</tr>
<tr>
<td>XCN_OID_OIWSEC_md5RSA(1.3.14.3.2.3)

</td>
<td>OIWSEC MD5 hashing algorithm combined with the RSA encryption algorithm.</td>
</tr>
</table>
 



The object is automatically initialized when an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>, <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>, or <a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object is initialized.

## -inheritance

The <b>IX509SignatureInformation</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IX509SignatureInformation</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certificate-enrollment-api-reference">Certificate Enrollment API</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>
