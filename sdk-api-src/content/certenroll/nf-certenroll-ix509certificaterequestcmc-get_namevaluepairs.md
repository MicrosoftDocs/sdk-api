---
UID: NF:certenroll.IX509CertificateRequestCmc.get_NameValuePairs
title: IX509CertificateRequestCmc::get_NameValuePairs (certenroll.h)
description: Retrieves an IX509NameValuePairs collection associated with a certificate request.
helpviewer_keywords: ["IX509CertificateRequestCmc interface [Security]","NameValuePairs property","IX509CertificateRequestCmc.NameValuePairs","IX509CertificateRequestCmc.get_NameValuePairs","IX509CertificateRequestCmc::NameValuePairs","IX509CertificateRequestCmc::get_NameValuePairs","NameValuePairs property [Security]","NameValuePairs property [Security]","IX509CertificateRequestCmc interface","certenroll/IX509CertificateRequestCmc::NameValuePairs","certenroll/IX509CertificateRequestCmc::get_NameValuePairs","get_NameValuePairs","security.ix509certificaterequestcmc_namevaluepairs_property"]
old-location: security\ix509certificaterequestcmc_namevaluepairs_property.htm
tech.root: security
ms.assetid: 3b98629e-a501-4ba0-8825-0cab7187d6f5
ms.date: 12/05/2018
ms.keywords: IX509CertificateRequestCmc interface [Security],NameValuePairs property, IX509CertificateRequestCmc.NameValuePairs, IX509CertificateRequestCmc.get_NameValuePairs, IX509CertificateRequestCmc::NameValuePairs, IX509CertificateRequestCmc::get_NameValuePairs, NameValuePairs property [Security], NameValuePairs property [Security],IX509CertificateRequestCmc interface, certenroll/IX509CertificateRequestCmc::NameValuePairs, certenroll/IX509CertificateRequestCmc::get_NameValuePairs, get_NameValuePairs, security.ix509certificaterequestcmc_namevaluepairs_property
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
 - IX509CertificateRequestCmc::get_NameValuePairs
 - certenroll/IX509CertificateRequestCmc::get_NameValuePairs
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
 - IX509CertificateRequestCmc.NameValuePairs
 - IX509CertificateRequestCmc.get_NameValuePairs
---

# IX509CertificateRequestCmc::get_NameValuePairs


## -description

The <b>NameValuePairs</b> property retrieves an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepairs">IX509NameValuePairs</a> collection associated with a certificate request.

This property is read-only.

## -parameters

## -remarks

For an example of a name-value pair in a CMC request object, see <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepair">IX509NameValuePair</a>. You must initialize the CMC request object before calling this property. For more information, see the following topics:<ul>
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