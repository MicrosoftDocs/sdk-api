---
UID: NF:certenroll.IX509CertificateRequestCmc.get_SuppressOids
title: IX509CertificateRequestCmc::get_SuppressOids (certenroll.h)
description: Retrieves a collection of extension or attribute object identifiers (OIDs) to be suppressed from the certificate during the encoding process.
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","SuppressOids property","IX509CertificateRequestCmc.SuppressOids","IX509CertificateRequestCmc.get_SuppressOids","IX509CertificateRequestCmc::SuppressOids","IX509CertificateRequestCmc::get_SuppressOids","SuppressOids property [Security]","SuppressOids property [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::SuppressOids","certenroll/IX509CertificateRequestCmc::get_SuppressOids","get_SuppressOids","security.ix509certificaterequestcmc_suppressoids_property"]
old-location: security\ix509certificaterequestcmc_suppressoids_property.htm
tech.root: security
ms.assetid: 6e0a8245-1bcc-413a-865a-8a6274dd55f5
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],SuppressOids property, IX509CertificateRequestCmc.SuppressOids, IX509CertificateRequestCmc.get_SuppressOids, IX509CertificateRequestCmc::SuppressOids, IX509CertificateRequestCmc::get_SuppressOids, SuppressOids property [Security], SuppressOids property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::SuppressOids, certenroll/IX509CertificateRequestCmc::get_SuppressOids, get_SuppressOids, security.ix509certificaterequestcmc_suppressoids_property
f1_keywords:
- certenroll/IX509CertificateRequestCmc.SuppressOids
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CertEnroll.dll
api_name:
- IX509CertificateRequestCmc.SuppressOids
- IX509CertificateRequestCmc.get_SuppressOids
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509CertificateRequestCmc::get_SuppressOids


## -description


The <b>SuppressOids</b> property retrieves a collection of extension or attribute <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) to be suppressed from the certificate during the encoding process.

This property is read-only.


## -parameters


## -remarks



Attributes and extensions are added to a certificate request when it is encoded or initialized. You can suppress the addition of default extensions and attributes by calling the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_suppressdefaults">SuppressDefaults</a> property. For a CMC request, only the XCN_OID_REQUEST_CLIENT_INFO
(<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeclientid">IX509AttributeClientId</a>) attribute is created by default. No extensions are added by default.

You must initialize the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a> object before calling this property. For more information, see any of the following methods:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-initialize">Initialize</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializedecode">InitializeDecode</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate">InitializeFromCertificate</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefrominnerrequest">InitializeFromInnerRequest</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestcmc-initializefrominnerrequesttemplatename">InitializeFromInnerRequestTemplateName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a>
 

 

