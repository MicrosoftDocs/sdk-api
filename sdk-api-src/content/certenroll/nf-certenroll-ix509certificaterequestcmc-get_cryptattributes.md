---
UID: NF:certenroll.IX509CertificateRequestCmc.get_CryptAttributes
title: IX509CertificateRequestCmc::get_CryptAttributes (certenroll.h)
description: Retrieves an ICryptAttributes collection of optional certificate attributes. (IX509CertificateRequestCmc.get_CryptAttributes)
helpviewer_keywords: ["CryptAttributes property [Security]","CryptAttributes property [Security]","IX509CertificateRequestCmc interface","IX509CertificateRequestCmc interface [Security]","CryptAttributes property","IX509CertificateRequestCmc.CryptAttributes","IX509CertificateRequestCmc.get_CryptAttributes","IX509CertificateRequestCmc::CryptAttributes","IX509CertificateRequestCmc::get_CryptAttributes","certenroll/IX509CertificateRequestCmc::CryptAttributes","certenroll/IX509CertificateRequestCmc::get_CryptAttributes","get_CryptAttributes","security.ix509certificaterequestcmc_cryptattributes_property"]
old-location: security\ix509certificaterequestcmc_cryptattributes_property.htm
tech.root: security
ms.assetid: 733d29d8-95ea-4193-99b0-a07fcf560435
ms.date: 12/05/2018
ms.keywords: CryptAttributes property [Security], CryptAttributes property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],CryptAttributes property, IX509CertificateRequestCmc.CryptAttributes, IX509CertificateRequestCmc.get_CryptAttributes, IX509CertificateRequestCmc::CryptAttributes, IX509CertificateRequestCmc::get_CryptAttributes, certenroll/IX509CertificateRequestCmc::CryptAttributes, certenroll/IX509CertificateRequestCmc::get_CryptAttributes, get_CryptAttributes, security.ix509certificaterequestcmc_cryptattributes_property
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
 - IX509CertificateRequestCmc::get_CryptAttributes
 - certenroll/IX509CertificateRequestCmc::get_CryptAttributes
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
 - IX509CertificateRequestCmc.CryptAttributes
 - IX509CertificateRequestCmc.get_CryptAttributes
---

# IX509CertificateRequestCmc::get_CryptAttributes


## -description

The <b>CryptAttributes</b> property retrieves an <a href="/windows/desktop/api/certenroll/nn-certenroll-icryptattributes">ICryptAttributes</a> collection of optional certificate attributes.

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
