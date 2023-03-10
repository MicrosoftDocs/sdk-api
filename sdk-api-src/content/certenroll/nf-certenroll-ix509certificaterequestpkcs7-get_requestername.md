---
UID: NF:certenroll.IX509CertificateRequestPkcs7.get_RequesterName
title: IX509CertificateRequestPkcs7::get_RequesterName (certenroll.h)
description: Specifies or retrieves a string that contains the Security Account Manager (SAM) name of the end-entity requesting the certificate. (Get)
helpviewer_keywords: ["IX509CertificateRequestPkcs7 interface [Security]","RequesterName property","IX509CertificateRequestPkcs7.RequesterName","IX509CertificateRequestPkcs7.get_RequesterName","IX509CertificateRequestPkcs7::RequesterName","IX509CertificateRequestPkcs7::get_RequesterName","IX509CertificateRequestPkcs7::put_RequesterName","RequesterName property [Security]","RequesterName property [Security]","IX509CertificateRequestPkcs7 interface","certenroll/IX509CertificateRequestPkcs7::RequesterName","certenroll/IX509CertificateRequestPkcs7::get_RequesterName","certenroll/IX509CertificateRequestPkcs7::put_RequesterName","get_RequesterName","security.ix509certificaterequestpkcs7_requestername_property"]
old-location: security\ix509certificaterequestpkcs7_requestername_property.htm
tech.root: security
ms.assetid: af85e976-cc79-4285-b553-a8001e84ec68
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs7 interface [Security],RequesterName property, IX509CertificateRequestPkcs7.RequesterName, IX509CertificateRequestPkcs7.get_RequesterName, IX509CertificateRequestPkcs7::RequesterName, IX509CertificateRequestPkcs7::get_RequesterName, IX509CertificateRequestPkcs7::put_RequesterName, RequesterName property [Security], RequesterName property [Security],IX509CertificateRequestPkcs7 interface, certenroll/IX509CertificateRequestPkcs7::RequesterName, certenroll/IX509CertificateRequestPkcs7::get_RequesterName, certenroll/IX509CertificateRequestPkcs7::put_RequesterName, get_RequesterName, security.ix509certificaterequestpkcs7_requestername_property
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
 - IX509CertificateRequestPkcs7::get_RequesterName
 - certenroll/IX509CertificateRequestPkcs7::get_RequesterName
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
 - IX509CertificateRequestPkcs7.RequesterName
 - IX509CertificateRequestPkcs7.get_RequesterName
 - IX509CertificateRequestPkcs7.put_RequesterName
---

# IX509CertificateRequestPkcs7::get_RequesterName


## -description

The <b>RequesterName</b> property specifies or retrieves a string that contains the Security Account Manager (SAM) name of the end-entity requesting the certificate. This property is web enabled for both input and output.

This property is read/write.

## -parameters

## -remarks

This property is only used when the enrollment agent is enrolling on behalf of another user. You must initialize the PKCS #7 request object before calling this property. For more information, see the following topics:<ul>
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
