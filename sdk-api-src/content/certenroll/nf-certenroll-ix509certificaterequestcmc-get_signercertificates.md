---
UID: NF:certenroll.IX509CertificateRequestCmc.get_SignerCertificates
title: IX509CertificateRequestCmc::get_SignerCertificates (certenroll.h)
description: Retrieves a collection of certificates used to sign the request.
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","SignerCertificates property","IX509CertificateRequestCmc.SignerCertificates","IX509CertificateRequestCmc.get_SignerCertificates","IX509CertificateRequestCmc::SignerCertificates","IX509CertificateRequestCmc::get_SignerCertificates","SignerCertificates property [Security]","SignerCertificates property [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::SignerCertificates","certenroll/IX509CertificateRequestCmc::get_SignerCertificates","get_SignerCertificates","security.ix509certificaterequestcmc_signercertificates_property"]
old-location: security\ix509certificaterequestcmc_signercertificates_property.htm
tech.root: security
ms.assetid: 0b963fe2-32bd-4f99-9d4f-b17cb2d65909
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],SignerCertificates property, IX509CertificateRequestCmc.SignerCertificates, IX509CertificateRequestCmc.get_SignerCertificates, IX509CertificateRequestCmc::SignerCertificates, IX509CertificateRequestCmc::get_SignerCertificates, SignerCertificates property [Security], SignerCertificates property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::SignerCertificates, certenroll/IX509CertificateRequestCmc::get_SignerCertificates, get_SignerCertificates, security.ix509certificaterequestcmc_signercertificates_property
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
 - IX509CertificateRequestCmc::get_SignerCertificates
 - certenroll/IX509CertificateRequestCmc::get_SignerCertificates
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
 - IX509CertificateRequestCmc.SignerCertificates
 - IX509CertificateRequestCmc.get_SignerCertificates
---

# IX509CertificateRequestCmc::get_SignerCertificates


## -description

The <b>SignerCertificates</b> property retrieves a collection of certificates used to sign the request.

This property is read-only.

## -parameters

## -remarks

A CMC request can have a primary signature plus zero or more certificate-based signatures. Certificate-based signatures can be included in a request if, for example, one or more additional parties must vouch for the identity of the entity requesting the new certificate. Call the <b>SignerCertificates</b> property to retrieve a collection of these additional certificate-based signatures.

The primary signature is typically created by using the private key that matches the public key in the inner PKCS #10 request object. Because the private key is usually created to enroll a new request in a certificate hierarchy, the primary signature is not certificate-based, and you must call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-get_signatureinformation">SignatureInformation</a> property to retrieve it.

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