---
UID: NF:certenroll.IX509AttributeCspProvider.get_Signature
title: IX509AttributeCspProvider::get_Signature (certenroll.h)
description: Retrieves the digital signature on the provider.
helpviewer_keywords: ["IX509AttributeCspProvider interface [Security]","Signature property","IX509AttributeCspProvider.Signature","IX509AttributeCspProvider.get_Signature","IX509AttributeCspProvider::Signature","IX509AttributeCspProvider::get_Signature","Signature property [Security]","Signature property [Security]","IX509AttributeCspProvider interface","certenroll/IX509AttributeCspProvider::Signature","certenroll/IX509AttributeCspProvider::get_Signature","get_Signature","security.ix509attributecspprovider_signature_property"]
old-location: security\ix509attributecspprovider_signature_property.htm
tech.root: security
ms.assetid: 06245293-b331-4963-a0cf-b7c604580908
ms.date: 12/05/2018
ms.keywords: IX509AttributeCspProvider interface [Security],Signature property, IX509AttributeCspProvider.Signature, IX509AttributeCspProvider.get_Signature, IX509AttributeCspProvider::Signature, IX509AttributeCspProvider::get_Signature, Signature property [Security], Signature property [Security],IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::Signature, certenroll/IX509AttributeCspProvider::get_Signature, get_Signature, security.ix509attributecspprovider_signature_property
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
 - IX509AttributeCspProvider::get_Signature
 - certenroll/IX509AttributeCspProvider::get_Signature
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
 - IX509AttributeCspProvider.Signature
 - IX509AttributeCspProvider.get_Signature
---

# IX509AttributeCspProvider::get_Signature


## -description

The <b>Signature</b> property retrieves the <a href="/windows/desktop/SecGloss/d-gly">digital signature</a> on the provider. The signature is contained in a byte array represented by a Unicode-encoded string.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-initializeencode">InitializeEncode</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-initializedecode">InitializeDecode</a> method to initialize the <b>Signature</b> property. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_keyspec">KeySpec</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_providername">ProviderName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributecspprovider">IX509AttributeCspProvider</a>