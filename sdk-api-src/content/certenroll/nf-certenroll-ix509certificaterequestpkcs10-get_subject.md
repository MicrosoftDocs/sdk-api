---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_Subject
title: IX509CertificateRequestPkcs10::get_Subject (certenroll.h)
description: Specifies or retrieves the X.500 distinguished name of the entity requesting the certificate. (Get)
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","Subject property","IX509CertificateRequestPkcs10.Subject","IX509CertificateRequestPkcs10.get_Subject","IX509CertificateRequestPkcs10::Subject","IX509CertificateRequestPkcs10::get_Subject","IX509CertificateRequestPkcs10::put_Subject","Subject property [Security]","Subject property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::Subject","certenroll/IX509CertificateRequestPkcs10::get_Subject","certenroll/IX509CertificateRequestPkcs10::put_Subject","get_Subject","security.ix509certificaterequestpkcs10_subject_property"]
old-location: security\ix509certificaterequestpkcs10_subject_property.htm
tech.root: security
ms.assetid: 7b521586-f2fc-4b2f-83ab-79f9b972f9a1
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],Subject property, IX509CertificateRequestPkcs10.Subject, IX509CertificateRequestPkcs10.get_Subject, IX509CertificateRequestPkcs10::Subject, IX509CertificateRequestPkcs10::get_Subject, IX509CertificateRequestPkcs10::put_Subject, Subject property [Security], Subject property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::Subject, certenroll/IX509CertificateRequestPkcs10::get_Subject, certenroll/IX509CertificateRequestPkcs10::put_Subject, get_Subject, security.ix509certificaterequestpkcs10_subject_property
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
 - IX509CertificateRequestPkcs10::get_Subject
 - certenroll/IX509CertificateRequestPkcs10::get_Subject
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
 - IX509CertificateRequestPkcs10.Subject
 - IX509CertificateRequestPkcs10.get_Subject
 - IX509CertificateRequestPkcs10.put_Subject
---

# IX509CertificateRequestPkcs10::get_Subject


## -description

The <b>Subject</b> property specifies or retrieves the X.500 distinguished name of the entity requesting the certificate. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

You must set this property before calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-encode">Encode</a> method, and you must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
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
