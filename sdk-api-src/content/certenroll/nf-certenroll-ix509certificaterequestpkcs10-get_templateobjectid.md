---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_TemplateObjectId
title: IX509CertificateRequestPkcs10::get_TemplateObjectId (certenroll.h)
description: Retrieves the object identifier (OID) of the template used to create the certificate request. (IX509CertificateRequestPkcs10.get_TemplateObjectId)
helpviewer_keywords: ["IX509CertificateRequestPkcs10 interface [Security]","TemplateObjectId property","IX509CertificateRequestPkcs10.TemplateObjectId","IX509CertificateRequestPkcs10.get_TemplateObjectId","IX509CertificateRequestPkcs10::TemplateObjectId","IX509CertificateRequestPkcs10::get_TemplateObjectId","TemplateObjectId property [Security]","TemplateObjectId property [Security]","IX509CertificateRequestPkcs10 interface","certenroll/IX509CertificateRequestPkcs10::TemplateObjectId","certenroll/IX509CertificateRequestPkcs10::get_TemplateObjectId","get_TemplateObjectId","security.ix509certificaterequestpkcs10_templateobjectid_property"]
old-location: security\ix509certificaterequestpkcs10_templateobjectid_property.htm
tech.root: security
ms.assetid: 490a34bc-08b3-4df2-8996-6137bea53420
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],TemplateObjectId property, IX509CertificateRequestPkcs10.TemplateObjectId, IX509CertificateRequestPkcs10.get_TemplateObjectId, IX509CertificateRequestPkcs10::TemplateObjectId, IX509CertificateRequestPkcs10::get_TemplateObjectId, TemplateObjectId property [Security], TemplateObjectId property [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::TemplateObjectId, certenroll/IX509CertificateRequestPkcs10::get_TemplateObjectId, get_TemplateObjectId, security.ix509certificaterequestpkcs10_templateobjectid_property
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
 - IX509CertificateRequestPkcs10::get_TemplateObjectId
 - certenroll/IX509CertificateRequestPkcs10::get_TemplateObjectId
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
 - IX509CertificateRequestPkcs10.TemplateObjectId
 - IX509CertificateRequestPkcs10.get_TemplateObjectId
---

# IX509CertificateRequestPkcs10::get_TemplateObjectId


## -description

The <b>TemplateObjectId</b> property retrieves the  <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the template used to create the certificate request.

This property is read-only.

## -parameters

## -remarks

The object identifier can be an OID for the Active Directory Common Name (CN) of the template. You must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> object before calling this property. For more information, see any of the following methods:<ul>
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
