---
UID: NF:certenroll.IX509CertificateRequestCmc.get_NullSigned
title: IX509CertificateRequestCmc::get_NullSigned (certenroll.h)
description: Retrieves a Boolean value that specifies whether the primary signature on the certificate request is null-signed.
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","NullSigned property","IX509CertificateRequestCmc.NullSigned","IX509CertificateRequestCmc.get_NullSigned","IX509CertificateRequestCmc::NullSigned","IX509CertificateRequestCmc::get_NullSigned","NullSigned property [Security]","NullSigned property [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::NullSigned","certenroll/IX509CertificateRequestCmc::get_NullSigned","get_NullSigned","security.ix509certificaterequestcmc_nullsigned_property"]
old-location: security\ix509certificaterequestcmc_nullsigned_property.htm
tech.root: security
ms.assetid: 99cefeed-caec-401e-bdcd-d167472b2cbd
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],NullSigned property, IX509CertificateRequestCmc.NullSigned, IX509CertificateRequestCmc.get_NullSigned, IX509CertificateRequestCmc::NullSigned, IX509CertificateRequestCmc::get_NullSigned, NullSigned property [Security], NullSigned property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::NullSigned, certenroll/IX509CertificateRequestCmc::get_NullSigned, get_NullSigned, security.ix509certificaterequestcmc_nullsigned_property
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
 - IX509CertificateRequestCmc::get_NullSigned
 - certenroll/IX509CertificateRequestCmc::get_NullSigned
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
 - IX509CertificateRequestCmc.NullSigned
 - IX509CertificateRequestCmc.get_NullSigned
---

# IX509CertificateRequestCmc::get_NullSigned


## -description

The <b>NullSigned</b> property retrieves a Boolean value that specifies whether the primary signature  on the certificate request is null-signed.

This property is read-only.

## -parameters

## -remarks

A null-signed certificate request is not really signed. That is, the request can be digested by using a digest algorithm such as SHA-1, but it is not encrypted with a public key algorithm such as RSA. This can be used when a private key is not available as is often the case when <a href="/windows/desktop/SecGloss/c-gly">certification authorities</a> are being cross-certified.

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