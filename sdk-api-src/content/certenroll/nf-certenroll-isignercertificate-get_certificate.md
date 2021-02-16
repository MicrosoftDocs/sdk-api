---
UID: NF:certenroll.ISignerCertificate.get_Certificate
title: ISignerCertificate::get_Certificate (certenroll.h)
description: Retrieves a Distinguished Encoding Rules (DER) encoded byte array that contains the certificate.
helpviewer_keywords: ["Certificate property [Security]","Certificate property [Security]","ISignerCertificate interface","ISignerCertificate interface [Security]","Certificate property","ISignerCertificate.Certificate","ISignerCertificate.get_Certificate","ISignerCertificate::Certificate","ISignerCertificate::get_Certificate","certenroll/ISignerCertificate::Certificate","certenroll/ISignerCertificate::get_Certificate","get_Certificate","security.isignercertificate_certificate_property"]
old-location: security\isignercertificate_certificate_property.htm
tech.root: security
ms.assetid: 7c7cc326-593d-4b2b-b8db-46aaf894279b
ms.date: 12/05/2018
ms.keywords: Certificate property [Security], Certificate property [Security],ISignerCertificate interface, ISignerCertificate interface [Security],Certificate property, ISignerCertificate.Certificate, ISignerCertificate.get_Certificate, ISignerCertificate::Certificate, ISignerCertificate::get_Certificate, certenroll/ISignerCertificate::Certificate, certenroll/ISignerCertificate::get_Certificate, get_Certificate, security.isignercertificate_certificate_property
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
 - ISignerCertificate::get_Certificate
 - certenroll/ISignerCertificate::get_Certificate
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
 - ISignerCertificate.Certificate
 - ISignerCertificate.get_Certificate
---

# ISignerCertificate::get_Certificate


## -description

The <b>Certificate</b> property retrieves a <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the certificate. The DER-encoded byte array is represented by a Unicode-encoded string.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-initialize">Initialize</a> method to specify the certificate. You can also call the following properties to retrieve information about the signing certificate object:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-put_pin">Pin</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_privatekey">PrivateKey</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_signatureinformation">SignatureInformation</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_silent">Silent</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-isignercertificate-get_uicontextmessage">UIContextMessage</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>