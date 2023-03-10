---
UID: NF:certenroll.IX509CertificateRequestCmc.get_TemplateObjectId
title: IX509CertificateRequestCmc::get_TemplateObjectId (certenroll.h)
description: Retrieves the object identifier (OID) of the template used to create the certificate request. (IX509CertificateRequestCmc.get_TemplateObjectId)
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","TemplateObjectId property","IX509CertificateRequestCmc.TemplateObjectId","IX509CertificateRequestCmc.get_TemplateObjectId","IX509CertificateRequestCmc::TemplateObjectId","IX509CertificateRequestCmc::get_TemplateObjectId","TemplateObjectId property [Security]","TemplateObjectId property [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::TemplateObjectId","certenroll/IX509CertificateRequestCmc::get_TemplateObjectId","get_TemplateObjectId","security.ix509certificaterequestcmc_templateobjectid_property"]
old-location: security\ix509certificaterequestcmc_templateobjectid_property.htm
tech.root: security
ms.assetid: 36a87e0e-d910-45a7-9850-512ff94e78b8
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],TemplateObjectId property, IX509CertificateRequestCmc.TemplateObjectId, IX509CertificateRequestCmc.get_TemplateObjectId, IX509CertificateRequestCmc::TemplateObjectId, IX509CertificateRequestCmc::get_TemplateObjectId, TemplateObjectId property [Security], TemplateObjectId property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::TemplateObjectId, certenroll/IX509CertificateRequestCmc::get_TemplateObjectId, get_TemplateObjectId, security.ix509certificaterequestcmc_templateobjectid_property
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
 - IX509CertificateRequestCmc::get_TemplateObjectId
 - certenroll/IX509CertificateRequestCmc::get_TemplateObjectId
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
 - IX509CertificateRequestCmc.TemplateObjectId
 - IX509CertificateRequestCmc.get_TemplateObjectId
---

# IX509CertificateRequestCmc::get_TemplateObjectId


## -description

The <b>TemplateObjectId</b> property retrieves the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the template used to create the certificate request.

This property is read-only.

## -parameters

## -remarks

The object identifier can be an OID for the Active Directory Common Name (CN) of the template. You must initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a> object before calling this property. For more information, see any of the following methods:<ul>
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
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename">InitializeFromInnerRequestTemplateName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>
