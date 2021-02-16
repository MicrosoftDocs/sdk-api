---
UID: NF:certenroll.ICertificatePolicy.get_PolicyQualifiers
title: ICertificatePolicy::get_PolicyQualifiers (certenroll.h)
description: Retrieves a collection of optional policy qualifiers that can be applied to a certificate policy.
helpviewer_keywords: ["ICertificatePolicy interface [Security]","PolicyQualifiers property","ICertificatePolicy.PolicyQualifiers","ICertificatePolicy.get_PolicyQualifiers","ICertificatePolicy::PolicyQualifiers","ICertificatePolicy::get_PolicyQualifiers","PolicyQualifiers property [Security]","PolicyQualifiers property [Security]","ICertificatePolicy interface","certenroll/ICertificatePolicy::PolicyQualifiers","certenroll/ICertificatePolicy::get_PolicyQualifiers","get_PolicyQualifiers","security.icertificatepolicy_policyqualifiers_property"]
old-location: security\icertificatepolicy_policyqualifiers_property.htm
tech.root: security
ms.assetid: 7955dfa1-70b2-4b6e-975f-c489a6284c5c
ms.date: 12/05/2018
ms.keywords: ICertificatePolicy interface [Security],PolicyQualifiers property, ICertificatePolicy.PolicyQualifiers, ICertificatePolicy.get_PolicyQualifiers, ICertificatePolicy::PolicyQualifiers, ICertificatePolicy::get_PolicyQualifiers, PolicyQualifiers property [Security], PolicyQualifiers property [Security],ICertificatePolicy interface, certenroll/ICertificatePolicy::PolicyQualifiers, certenroll/ICertificatePolicy::get_PolicyQualifiers, get_PolicyQualifiers, security.icertificatepolicy_policyqualifiers_property
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
 - ICertificatePolicy::get_PolicyQualifiers
 - certenroll/ICertificatePolicy::get_PolicyQualifiers
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
 - ICertificatePolicy.PolicyQualifiers
 - ICertificatePolicy.get_PolicyQualifiers
---

# ICertificatePolicy::get_PolicyQualifiers


## -description

The <b>PolicyQualifiers</b> property retrieves a collection of optional policy qualifiers that can be applied to a certificate policy.

This property is read-only.

## -parameters

## -remarks

An empty <a href="/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifiers">IPolicyQualifiers</a> object is created when you call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertificatepolicy-initialize">Initialize</a> method. You can call the <b>PolicyQualifiers</b> property to retrieve this object and specify qualifying information for the policy. Policy qualifiers only apply if you are creating a <b>CertificatePolicies</b> extension. For more information, see the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a>