---
UID: NF:certenroll.IX509CertificateRequestCmc.get_CriticalExtensions
title: IX509CertificateRequestCmc::get_CriticalExtensions (certenroll.h)
description: Retrieves an IObjectIds collection that identifies the version 3 certificate extensions marked as critical. (IX509CertificateRequestCmc.get_CriticalExtensions)
helpviewer_keywords: ["CriticalExtensions property [Security]","CriticalExtensions property [Security]","IX509CertificateRequestCmc interface","IX509CertificateRequestCmc interface [Security]","CriticalExtensions property","IX509CertificateRequestCmc.CriticalExtensions","IX509CertificateRequestCmc.get_CriticalExtensions","IX509CertificateRequestCmc::CriticalExtensions","IX509CertificateRequestCmc::get_CriticalExtensions","certenroll/IX509CertificateRequestCmc::CriticalExtensions","certenroll/IX509CertificateRequestCmc::get_CriticalExtensions","get_CriticalExtensions","security.ix509certificaterequestcmc_criticalextensions_property"]
old-location: security\ix509certificaterequestcmc_criticalextensions_property.htm
tech.root: security
ms.assetid: 06c5d148-eecc-45db-9d82-ec56c226ffed
ms.date: 12/05/2018
ms.keywords: CriticalExtensions property [Security], CriticalExtensions property [Security],IX509CertificateRequestCmc interface, IX509CertificateRequestCmc interface [Security],CriticalExtensions property, IX509CertificateRequestCmc.CriticalExtensions, IX509CertificateRequestCmc.get_CriticalExtensions, IX509CertificateRequestCmc::CriticalExtensions, IX509CertificateRequestCmc::get_CriticalExtensions, certenroll/IX509CertificateRequestCmc::CriticalExtensions, certenroll/IX509CertificateRequestCmc::get_CriticalExtensions, get_CriticalExtensions, security.ix509certificaterequestcmc_criticalextensions_property
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
 - IX509CertificateRequestCmc::get_CriticalExtensions
 - certenroll/IX509CertificateRequestCmc::get_CriticalExtensions
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
 - IX509CertificateRequestCmc.CriticalExtensions
 - IX509CertificateRequestCmc.get_CriticalExtensions
---

# IX509CertificateRequestCmc::get_CriticalExtensions


## -description

The <b>CriticalExtensions</b> property retrieves an <a href="/windows/desktop/api/certenroll/nn-certenroll-iobjectids">IObjectIds</a> collection that identifies the version 3 certificate extensions marked as critical.

This property is read-only.

## -parameters

## -remarks

The extension criticality indicates to an application that uses certificates whether it can ignore the extension. You must initialize the CMC request object before calling this property. For more information, see the following topics:

<ul>
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
