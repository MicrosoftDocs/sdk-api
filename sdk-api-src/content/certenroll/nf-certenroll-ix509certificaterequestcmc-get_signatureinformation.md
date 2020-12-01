---
UID: NF:certenroll.IX509CertificateRequestCmc.get_SignatureInformation
title: IX509CertificateRequestCmc::get_SignatureInformation (certenroll.h)
description: Retrieves the IX509SignatureInformation object that contains information about the primary signature used to sign the certificate request.
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","SignatureInformation property","IX509CertificateRequestCmc.SignatureInformation","IX509CertificateRequestCmc.get_SignatureInformation","IX509CertificateRequestCmc::SignatureInformation","IX509CertificateRequestCmc::get_SignatureInformation","SignatureInformation property [Security]","SignatureInformation property [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::SignatureInformation","certenroll/IX509CertificateRequestCmc::get_SignatureInformation","get_SignatureInformation","security.ix509certificaterequestcmc_signatureinformation_property"]
old-location: security\ix509certificaterequestcmc_signatureinformation_property.htm
tech.root: security
ms.assetid: cd5353b4-b1dd-495f-ae75-c6e14edbb8f9
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],SignatureInformation property, IX509CertificateRequestCmc.SignatureInformation, IX509CertificateRequestCmc.get_SignatureInformation, IX509CertificateRequestCmc::SignatureInformation, IX509CertificateRequestCmc::get_SignatureInformation, SignatureInformation property [Security], SignatureInformation property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::SignatureInformation, certenroll/IX509CertificateRequestCmc::get_SignatureInformation, get_SignatureInformation, security.ix509certificaterequestcmc_signatureinformation_property
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
 - IX509CertificateRequestCmc::get_SignatureInformation
 - certenroll/IX509CertificateRequestCmc::get_SignatureInformation
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
 - IX509CertificateRequestCmc.SignatureInformation
 - IX509CertificateRequestCmc.get_SignatureInformation
---

# IX509CertificateRequestCmc::get_SignatureInformation


## -description

The <b>SignatureInformation</b> property retrieves the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object that contains information about the primary signature used to sign the certificate request. This property is web enabled.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object contains information about the hash, public key and signature algorithms used for the primary signature that signs the certificate request. A CMC request can have a primary signature plus zero or more certificate-based signatures. Certificate-based signatures can be included in a request if, for example, one or more additional parties must vouch for the identity of the entity requesting the new certificate. You can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_signercertificates">SignerCertificates</a> property to retrieve a collection of these additional certificate-based signatures.

The primary signature is typically created by using the private key that matches the public key in the inner PKCS #10 request object. Because the private key is usually created to enroll a new request in a certificate hierarchy, the primary signature is not certificate-based, and you must call the <b>SignatureInformation</b> property to retrieve it.

 If the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object does not exist when the <b>SignatureInformation</b> property is called or creation of the signature was deferred during initialization, this property:<ul>
<li>Retrieves the innermost PKCS #10 request object.</li>
<li>Retrieves and duplicates the signature information from the inner request.</li>
<li>Attempts to retrieve the private key associated with the inner PKCS #10 and sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_nullsigned">NullSigned</a> property if no private key can be found.</li>
<li>Retrieves the hash algorithm, if one is specified, from the template associated with the inner request and sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm">HashAlgorithm</a> property.</li>
<li>Retrieves the asymmetric algorithm, if one is specified, from the private key associated with the inner request and sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_publickeyalgorithm">PublicKeyAlgorithm</a> property.</li>
<li>Retrieves the private key flags from the template and sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_alternatesignaturealgorithm">AlternateSignatureAlgorithm</a> if appropriate </li>
</ul>


You must initialize the CMC request object before calling this property. For more information, see the following topics:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-initialize">Initialize</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefrominnerrequest">InitializeFromInnerRequest</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename">InitializeFromInnerRequestTemplateName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>