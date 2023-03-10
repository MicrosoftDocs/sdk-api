---
UID: NF:certenroll.IX509CertificateRequestCertificate.get_Issuer
title: IX509CertificateRequestCertificate::get_Issuer (certenroll.h)
description: Specifies or retrieves the name of the certificate issuer. (Get)
helpviewer_keywords: ["IX509CertificateRequestCertificate interface [Security]","Issuer property","IX509CertificateRequestCertificate.Issuer","IX509CertificateRequestCertificate.get_Issuer","IX509CertificateRequestCertificate::Issuer","IX509CertificateRequestCertificate::get_Issuer","IX509CertificateRequestCertificate::put_Issuer","Issuer property [Security]","Issuer property [Security]","IX509CertificateRequestCertificate interface","certenroll/IX509CertificateRequestCertificate::Issuer","certenroll/IX509CertificateRequestCertificate::get_Issuer","certenroll/IX509CertificateRequestCertificate::put_Issuer","get_Issuer","security.ix509certificaterequestcertificate_issuer_property"]
old-location: security\ix509certificaterequestcertificate_issuer_property.htm
tech.root: security
ms.assetid: cf07a0ed-8657-4044-8dcd-fcd350af20ee
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCertificate interface [Security],Issuer property, IX509CertificateRequestCertificate.Issuer, IX509CertificateRequestCertificate.get_Issuer, IX509CertificateRequestCertificate::Issuer, IX509CertificateRequestCertificate::get_Issuer, IX509CertificateRequestCertificate::put_Issuer, Issuer property [Security], Issuer property [Security],IX509CertificateRequestCertificate interface, certenroll/IX509CertificateRequestCertificate::Issuer, certenroll/IX509CertificateRequestCertificate::get_Issuer, certenroll/IX509CertificateRequestCertificate::put_Issuer, get_Issuer, security.ix509certificaterequestcertificate_issuer_property
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
 - IX509CertificateRequestCertificate::get_Issuer
 - certenroll/IX509CertificateRequestCertificate::get_Issuer
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
 - IX509CertificateRequestCertificate.Issuer
 - IX509CertificateRequestCertificate.get_Issuer
 - IX509CertificateRequestCertificate.put_Issuer
---

# IX509CertificateRequestCertificate::get_Issuer


## -description

The <b>Issuer</b> property specifies or retrieves the name of the certificate issuer.

This property is read/write.

## -parameters

## -remarks

If you do not specify this property before calling <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a>, the property value is set by using the subject of the signing certificate. If no signing certificate was supplied, the property value is set by using the subject of the request object.

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

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix500distinguishedname">IX500DistinguishedName</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a>
