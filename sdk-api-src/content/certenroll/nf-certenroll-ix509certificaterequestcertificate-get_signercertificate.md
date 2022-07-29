---
UID: NF:certenroll.IX509CertificateRequestCertificate.get_SignerCertificate
title: IX509CertificateRequestCertificate::get_SignerCertificate (certenroll.h)
description: Specifies or retrieves the ISignerCertificate object used to sign the certificate. (Get)
helpviewer_keywords: ["IX509CertificateRequestCertificate interface [Security]","SignerCertificate property","IX509CertificateRequestCertificate.SignerCertificate","IX509CertificateRequestCertificate.get_SignerCertificate","IX509CertificateRequestCertificate::SignerCertificate","IX509CertificateRequestCertificate::get_SignerCertificate","IX509CertificateRequestCertificate::put_SignerCertificate","SignerCertificate property [Security]","SignerCertificate property [Security]","IX509CertificateRequestCertificate interface","certenroll/IX509CertificateRequestCertificate::SignerCertificate","certenroll/IX509CertificateRequestCertificate::get_SignerCertificate","certenroll/IX509CertificateRequestCertificate::put_SignerCertificate","get_SignerCertificate","security.ix509certificaterequestcertificate_signercertificate_property"]
old-location: security\ix509certificaterequestcertificate_signercertificate_property.htm
tech.root: security
ms.assetid: e3a66651-aa0d-4dbb-afb1-f2492e27fec1
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCertificate interface [Security],SignerCertificate property, IX509CertificateRequestCertificate.SignerCertificate, IX509CertificateRequestCertificate.get_SignerCertificate, IX509CertificateRequestCertificate::SignerCertificate, IX509CertificateRequestCertificate::get_SignerCertificate, IX509CertificateRequestCertificate::put_SignerCertificate, SignerCertificate property [Security], SignerCertificate property [Security],IX509CertificateRequestCertificate interface, certenroll/IX509CertificateRequestCertificate::SignerCertificate, certenroll/IX509CertificateRequestCertificate::get_SignerCertificate, certenroll/IX509CertificateRequestCertificate::put_SignerCertificate, get_SignerCertificate, security.ix509certificaterequestcertificate_signercertificate_property
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
 - IX509CertificateRequestCertificate::get_SignerCertificate
 - certenroll/IX509CertificateRequestCertificate::get_SignerCertificate
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
 - IX509CertificateRequestCertificate.SignerCertificate
 - IX509CertificateRequestCertificate.get_SignerCertificate
 - IX509CertificateRequestCertificate.put_SignerCertificate
---

# IX509CertificateRequestCertificate::get_SignerCertificate


## -description

The <b>SignerCertificate</b> property specifies or retrieves the  <a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object used to sign the certificate.

This property is read/write.

## -parameters

## -remarks

You can set this property if you are not creating a self-signed certificate. If you do not specify the  property value before calling  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a>, the private key associated with the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a> object is used to sign the certificate, and the name of the issuer is set, by default, to the subject name.

You must initialize the request object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-initialize">Initialize</a>
</li>
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

<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>
