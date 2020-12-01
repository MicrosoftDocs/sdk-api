---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_NullSigned
title: IX509CertificateRequestPkcs10::get_NullSigned (certenroll.h)
description: Retrieves a Boolean value that indicates whether the certificate request is null-signed.
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","NullSigned property","IX509CertificateRequestPkcs10.NullSigned","IX509CertificateRequestPkcs10.get_NullSigned","IX509CertificateRequestPkcs10::NullSigned","IX509CertificateRequestPkcs10::get_NullSigned","NullSigned property [Security]","NullSigned property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::NullSigned","certenroll/IX509CertificateRequestPkcs10::get_NullSigned","get_NullSigned","security.ix509certificaterequestpkcs10_nullsigned_property"]
old-location: security\ix509certificaterequestpkcs10_nullsigned_property.htm
tech.root: security
ms.assetid: 2420f5ef-2cd7-498d-892a-2b99c524d629
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],NullSigned property, IX509CertificateRequestPkcs10.NullSigned, IX509CertificateRequestPkcs10.get_NullSigned, IX509CertificateRequestPkcs10::NullSigned, IX509CertificateRequestPkcs10::get_NullSigned, NullSigned property [Security], NullSigned property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::NullSigned, certenroll/IX509CertificateRequestPkcs10::get_NullSigned, get_NullSigned, security.ix509certificaterequestpkcs10_nullsigned_property
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
 - IX509CertificateRequestPkcs10::get_NullSigned
 - certenroll/IX509CertificateRequestPkcs10::get_NullSigned
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
 - IX509CertificateRequestPkcs10.NullSigned
 - IX509CertificateRequestPkcs10.get_NullSigned
---

# IX509CertificateRequestPkcs10::get_NullSigned


## -description

The <b>NullSigned</b> property retrieves a Boolean value that indicates whether the certificate request is null-signed.

This property is read-only.

## -parameters

## -remarks

A null-signed PKCS #10 certificate request is not really signed. That is, the signature is a hash created by using a digest algorithm such as SHA-1, but the request is not encrypted with a public key algorithm such as RSA. This can be used when a private key is not available as is often the case when <a href="/windows/desktop/SecGloss/c-gly">certification authorities</a> are being cross-certified. For more information, see the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a> method.

 You must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromprivatekey">InitializeFromPrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefrompublickey">InitializeFromPublicKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a>