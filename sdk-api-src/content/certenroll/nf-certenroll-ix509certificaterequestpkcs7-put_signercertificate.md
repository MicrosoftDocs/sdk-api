---
UID: NF:certenroll.IX509CertificateRequestPkcs7.put_SignerCertificate
title: IX509CertificateRequestPkcs7::put_SignerCertificate (certenroll.h)
description: Specifies or retrieves a certificate used to sign the certificate request. (Put)
helpviewer_keywords: ["IX509CertificateRequestPkcs7 interface [Security]","SignerCertificate property","IX509CertificateRequestPkcs7.SignerCertificate","IX509CertificateRequestPkcs7.put_SignerCertificate","IX509CertificateRequestPkcs7::SignerCertificate","IX509CertificateRequestPkcs7::get_SignerCertificate","IX509CertificateRequestPkcs7::put_SignerCertificate","SignerCertificate property [Security]","SignerCertificate property [Security]","IX509CertificateRequestPkcs7 interface","certenroll/IX509CertificateRequestPkcs7::SignerCertificate","certenroll/IX509CertificateRequestPkcs7::get_SignerCertificate","certenroll/IX509CertificateRequestPkcs7::put_SignerCertificate","put_SignerCertificate","security.ix509certificaterequestpkcs7_signercertificate_property"]
old-location: security\ix509certificaterequestpkcs7_signercertificate_property.htm
tech.root: security
ms.assetid: 5d93aad0-6b93-4508-9bf0-82f673585ead
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs7 interface [Security],SignerCertificate property, IX509CertificateRequestPkcs7.SignerCertificate, IX509CertificateRequestPkcs7.put_SignerCertificate, IX509CertificateRequestPkcs7::SignerCertificate, IX509CertificateRequestPkcs7::get_SignerCertificate, IX509CertificateRequestPkcs7::put_SignerCertificate, SignerCertificate property [Security], SignerCertificate property [Security],IX509CertificateRequestPkcs7 interface, certenroll/IX509CertificateRequestPkcs7::SignerCertificate, certenroll/IX509CertificateRequestPkcs7::get_SignerCertificate, certenroll/IX509CertificateRequestPkcs7::put_SignerCertificate, put_SignerCertificate, security.ix509certificaterequestpkcs7_signercertificate_property
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
 - IX509CertificateRequestPkcs7::put_SignerCertificate
 - certenroll/IX509CertificateRequestPkcs7::put_SignerCertificate
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
 - IX509CertificateRequestPkcs7.SignerCertificate
 - IX509CertificateRequestPkcs7.get_SignerCertificate
 - IX509CertificateRequestPkcs7.put_SignerCertificate
---

# IX509CertificateRequestPkcs7::put_SignerCertificate


## -description

The <b>SignerCertificate</b> property specifies or retrieves a  certificate used to sign the certificate request.

This property is read/write.

## -parameters

## -remarks

You must initialize the PKCS #7 request object before calling this property. For more information, see the following topics:<ul>
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
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a>
