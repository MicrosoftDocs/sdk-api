---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_SignatureInformation
title: IX509CertificateRequestPkcs10::get_SignatureInformation (certenroll.h)
description: Retrieves the IX509SignatureInformation object that contains information about the certificate request signature.
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","SignatureInformation property","IX509CertificateRequestPkcs10.SignatureInformation","IX509CertificateRequestPkcs10.get_SignatureInformation","IX509CertificateRequestPkcs10::SignatureInformation","IX509CertificateRequestPkcs10::get_SignatureInformation","SignatureInformation property [Security]","SignatureInformation property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::SignatureInformation","certenroll/IX509CertificateRequestPkcs10::get_SignatureInformation","get_SignatureInformation","security.ix509certificaterequestpkcs10_signatureinformation_property"]
old-location: security\ix509certificaterequestpkcs10_signatureinformation_property.htm
tech.root: security
ms.assetid: d90a8b82-a4d7-4d31-bcd0-293572a2bdd2
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],SignatureInformation property, IX509CertificateRequestPkcs10.SignatureInformation, IX509CertificateRequestPkcs10.get_SignatureInformation, IX509CertificateRequestPkcs10::SignatureInformation, IX509CertificateRequestPkcs10::get_SignatureInformation, SignatureInformation property [Security], SignatureInformation property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::SignatureInformation, certenroll/IX509CertificateRequestPkcs10::get_SignatureInformation, get_SignatureInformation, security.ix509certificaterequestpkcs10_signatureinformation_property
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
 - IX509CertificateRequestPkcs10::get_SignatureInformation
 - certenroll/IX509CertificateRequestPkcs10::get_SignatureInformation
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
 - IX509CertificateRequestPkcs10.SignatureInformation
 - IX509CertificateRequestPkcs10.get_SignatureInformation
---

# IX509CertificateRequestPkcs10::get_SignatureInformation


## -description

The <b>SignatureInformation</b> property retrieves the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object that contains information about the certificate request signature. This property is web enabled.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509signatureinformation">IX509SignatureInformation</a> object contains information about the hash, public key and signature algorithms used to sign the certificate request. If no <b>IX509SignatureInformation</b> object has been associated with the request, this property attempts to create one and use the private key to set the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509signatureinformation-get_publickeyalgorithm">PublicKeyAlgorithm</a> property.

 You must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object and call  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> before calling this property. For more information, see any of the following methods:<ul>
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