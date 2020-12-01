---
UID: NF:certenroll.IX509AttributeCspProvider.get_KeySpec
title: IX509AttributeCspProvider::get_KeySpec (certenroll.h)
description: Retrieves a value that identifies whether the key pair stored by the provider or key container is used for encryption or for signing content.
helpviewer_keywords: ["IX509AttributeCspProvider interface [Security]","KeySpec property","IX509AttributeCspProvider.KeySpec","IX509AttributeCspProvider.get_KeySpec","IX509AttributeCspProvider::KeySpec","IX509AttributeCspProvider::get_KeySpec","KeySpec property [Security]","KeySpec property [Security]","IX509AttributeCspProvider interface","certenroll/IX509AttributeCspProvider::KeySpec","certenroll/IX509AttributeCspProvider::get_KeySpec","get_KeySpec","security.ix509attributecspprovider_keyspec_property"]
old-location: security\ix509attributecspprovider_keyspec_property.htm
tech.root: security
ms.assetid: 4bb04097-9e6c-4b15-852e-be86d21637bf
ms.date: 12/05/2018
ms.keywords: IX509AttributeCspProvider interface [Security],KeySpec property, IX509AttributeCspProvider.KeySpec, IX509AttributeCspProvider.get_KeySpec, IX509AttributeCspProvider::KeySpec, IX509AttributeCspProvider::get_KeySpec, KeySpec property [Security], KeySpec property [Security],IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::KeySpec, certenroll/IX509AttributeCspProvider::get_KeySpec, get_KeySpec, security.ix509attributecspprovider_keyspec_property
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
 - IX509AttributeCspProvider::get_KeySpec
 - certenroll/IX509AttributeCspProvider::get_KeySpec
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
 - IX509AttributeCspProvider.KeySpec
 - IX509AttributeCspProvider.get_KeySpec
---

# IX509AttributeCspProvider::get_KeySpec


## -description

The <b>KeySpec</b> property retrieves a value that identifies whether the key pair stored by the provider or key container is used for encryption or for signing content.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-initializeencode">InitializeEncode</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-initializedecode">InitializeDecode</a> method to initialize the <b>KeySpec</b> property. You can also call the following properties to retrieve raw data:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_providername">ProviderName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_signature">Signature</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributecspprovider">IX509AttributeCspProvider</a>