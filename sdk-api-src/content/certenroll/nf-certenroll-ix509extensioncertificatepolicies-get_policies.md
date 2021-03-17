---
UID: NF:certenroll.IX509ExtensionCertificatePolicies.get_Policies
title: IX509ExtensionCertificatePolicies::get_Policies (certenroll.h)
description: Retrieves a collection of certificate policies.
helpviewer_keywords: ["IX509ExtensionCertificatePolicies interface [Security]","Policies property","IX509ExtensionCertificatePolicies.Policies","IX509ExtensionCertificatePolicies.get_Policies","IX509ExtensionCertificatePolicies::Policies","IX509ExtensionCertificatePolicies::get_Policies","Policies property [Security]","Policies property [Security]","IX509ExtensionCertificatePolicies interface","certenroll/IX509ExtensionCertificatePolicies::Policies","certenroll/IX509ExtensionCertificatePolicies::get_Policies","get_Policies","security.ix509extensioncertificatepolicies_policies_property"]
old-location: security\ix509extensioncertificatepolicies_policies_property.htm
tech.root: security
ms.assetid: eefb515d-62dc-4ad7-b0c4-c65a4da5742e
ms.date: 12/05/2018
ms.keywords: IX509ExtensionCertificatePolicies interface [Security],Policies property, IX509ExtensionCertificatePolicies.Policies, IX509ExtensionCertificatePolicies.get_Policies, IX509ExtensionCertificatePolicies::Policies, IX509ExtensionCertificatePolicies::get_Policies, Policies property [Security], Policies property [Security],IX509ExtensionCertificatePolicies interface, certenroll/IX509ExtensionCertificatePolicies::Policies, certenroll/IX509ExtensionCertificatePolicies::get_Policies, get_Policies, security.ix509extensioncertificatepolicies_policies_property
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
 - IX509ExtensionCertificatePolicies::get_Policies
 - certenroll/IX509ExtensionCertificatePolicies::get_Policies
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
 - IX509ExtensionCertificatePolicies.Policies
 - IX509ExtensionCertificatePolicies.get_Policies
---

# IX509ExtensionCertificatePolicies::get_Policies


## -description

The <b>Policies</b> property retrieves a collection of certificate policies.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensioncertificatepolicies-initializeencode">InitializeEncode</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensioncertificatepolicies-initializedecode">InitializeDecode</a> method to initialize the collection.  You can also call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property to retrieve the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) associated with the extension.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensioncertificatepolicies">IX509ExtensionCertificatePolicies</a>