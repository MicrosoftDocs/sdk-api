---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_OldCertificate
title: IX509CertificateRequestPkcs10::get_OldCertificate (certenroll.h)
description: Retrieves the certificate passed to the InitializeFromCertificate method.
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","OldCertificate property","IX509CertificateRequestPkcs10.OldCertificate","IX509CertificateRequestPkcs10.get_OldCertificate","IX509CertificateRequestPkcs10::OldCertificate","IX509CertificateRequestPkcs10::get_OldCertificate","OldCertificate property [Security]","OldCertificate property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::OldCertificate","certenroll/IX509CertificateRequestPkcs10::get_OldCertificate","get_OldCertificate","security.ix509certificaterequestpkcs10_oldcertificate_property"]
old-location: security\ix509certificaterequestpkcs10_oldcertificate_property.htm
tech.root: security
ms.assetid: 8bb15b5c-e642-477d-bcec-772748e336ef
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],OldCertificate property, IX509CertificateRequestPkcs10.OldCertificate, IX509CertificateRequestPkcs10.get_OldCertificate, IX509CertificateRequestPkcs10::OldCertificate, IX509CertificateRequestPkcs10::get_OldCertificate, OldCertificate property [Security], OldCertificate property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::OldCertificate, certenroll/IX509CertificateRequestPkcs10::get_OldCertificate, get_OldCertificate, security.ix509certificaterequestpkcs10_oldcertificate_property
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
 - IX509CertificateRequestPkcs10::get_OldCertificate
 - certenroll/IX509CertificateRequestPkcs10::get_OldCertificate
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
 - IX509CertificateRequestPkcs10.OldCertificate
 - IX509CertificateRequestPkcs10.get_OldCertificate
---

# IX509CertificateRequestPkcs10::get_OldCertificate


## -description

The <b>OldCertificate</b> property retrieves the certificate passed to the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate">InitializeFromCertificate</a> method.  The certificate is contained in a byte array encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard. The DER-encoded byte array is represented by a string that is either a pure binary sequence or is Unicode encoded.

This property is read-only.

## -parameters

## -remarks

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