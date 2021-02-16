---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_PublicKey
title: IX509CertificateRequestPkcs10::get_PublicKey (certenroll.h)
description: Retrieves the IX509PublicKey object that contains the public key included in the certificate request.
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","PublicKey property","IX509CertificateRequestPkcs10.PublicKey","IX509CertificateRequestPkcs10.get_PublicKey","IX509CertificateRequestPkcs10::PublicKey","IX509CertificateRequestPkcs10::get_PublicKey","PublicKey property [Security]","PublicKey property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::PublicKey","certenroll/IX509CertificateRequestPkcs10::get_PublicKey","get_PublicKey","security.ix509certificaterequestpkcs10_publickey_property"]
old-location: security\ix509certificaterequestpkcs10_publickey_property.htm
tech.root: security
ms.assetid: 9f9d05d8-9bc5-441e-8409-498ee9d20c25
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],PublicKey property, IX509CertificateRequestPkcs10.PublicKey, IX509CertificateRequestPkcs10.get_PublicKey, IX509CertificateRequestPkcs10::PublicKey, IX509CertificateRequestPkcs10::get_PublicKey, PublicKey property [Security], PublicKey property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::PublicKey, certenroll/IX509CertificateRequestPkcs10::get_PublicKey, get_PublicKey, security.ix509certificaterequestpkcs10_publickey_property
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
 - IX509CertificateRequestPkcs10::get_PublicKey
 - certenroll/IX509CertificateRequestPkcs10::get_PublicKey
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
 - IX509CertificateRequestPkcs10.PublicKey
 - IX509CertificateRequestPkcs10.get_PublicKey
---

# IX509CertificateRequestPkcs10::get_PublicKey


## -description

The <b>PublicKey</b> property retrieves the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509publickey">IX509PublicKey</a> object that contains the public key included in the certificate request.

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