---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_Signature
title: IX509CertificateRequestPkcs10::get_Signature (certenroll.h)
description: Retrieves the request signature created by the Encode method.
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","Signature property","IX509CertificateRequestPkcs10.Signature","IX509CertificateRequestPkcs10.get_Signature","IX509CertificateRequestPkcs10::Signature","IX509CertificateRequestPkcs10::get_Signature","Signature property [Security]","Signature property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::Signature","certenroll/IX509CertificateRequestPkcs10::get_Signature","get_Signature","security.ix509certificaterequestpkcs10_signature_property"]
old-location: security\ix509certificaterequestpkcs10_signature_property.htm
tech.root: security
ms.assetid: ee6ad3c7-2d31-4a12-ad37-ee6e1071b665
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],Signature property, IX509CertificateRequestPkcs10.Signature, IX509CertificateRequestPkcs10.get_Signature, IX509CertificateRequestPkcs10::Signature, IX509CertificateRequestPkcs10::get_Signature, Signature property [Security], Signature property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::Signature, certenroll/IX509CertificateRequestPkcs10::get_Signature, get_Signature, security.ix509certificaterequestpkcs10_signature_property
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
 - IX509CertificateRequestPkcs10::get_Signature
 - certenroll/IX509CertificateRequestPkcs10::get_Signature
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
 - IX509CertificateRequestPkcs10.Signature
 - IX509CertificateRequestPkcs10.get_Signature
---

# IX509CertificateRequestPkcs10::get_Signature


## -description

The <b>Signature</b> property retrieves the request signature created by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method. The signature is contained in a byte array encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard. The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method creates a DER-encoded and signed certificate request which it saves internally as a byte array. You can use the <b>Signature</b> property to retrieve a byte array that contains the signature.

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