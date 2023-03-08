---
UID: NF:certenroll.IX509CertificateRequestCmc.get_X509Extensions
title: IX509CertificateRequestCmc::get_X509Extensions (certenroll.h)
description: Retrieves a collection of the extensions included in the certificate request. (IX509CertificateRequestCmc.get_X509Extensions)
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","X509Extensions property","IX509CertificateRequestCmc.X509Extensions","IX509CertificateRequestCmc.get_X509Extensions","IX509CertificateRequestCmc::X509Extensions","IX509CertificateRequestCmc::get_X509Extensions","X509Extensions property [Security]","X509Extensions property [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::X509Extensions","certenroll/IX509CertificateRequestCmc::get_X509Extensions","get_X509Extensions","security.ix509certificaterequestcmc_x509extensions_property"]
old-location: security\ix509certificaterequestcmc_x509extensions_property.htm
tech.root: security
ms.assetid: 75eae625-5c41-4eef-aacd-bd1681286b2b
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],X509Extensions property, IX509CertificateRequestCmc.X509Extensions, IX509CertificateRequestCmc.get_X509Extensions, IX509CertificateRequestCmc::X509Extensions, IX509CertificateRequestCmc::get_X509Extensions, X509Extensions property [Security], X509Extensions property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::X509Extensions, certenroll/IX509CertificateRequestCmc::get_X509Extensions, get_X509Extensions, security.ix509certificaterequestcmc_x509extensions_property
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
 - IX509CertificateRequestCmc::get_X509Extensions
 - certenroll/IX509CertificateRequestCmc::get_X509Extensions
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
 - IX509CertificateRequestCmc.X509Extensions
 - IX509CertificateRequestCmc.get_X509Extensions
---

# IX509CertificateRequestCmc::get_X509Extensions


## -description

The <b>X509Extensions</b> property retrieves a collection of the extensions included in the certificate request.

This property is read-only.

## -parameters

## -remarks

You must initialize the CMC request object before calling this property. For more information, see the following topics:<ul>
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
