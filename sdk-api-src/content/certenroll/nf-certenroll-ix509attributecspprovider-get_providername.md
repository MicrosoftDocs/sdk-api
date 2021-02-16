---
UID: NF:certenroll.IX509AttributeCspProvider.get_ProviderName
title: IX509AttributeCspProvider::get_ProviderName (certenroll.h)
description: Retrieves the provider name.
helpviewer_keywords: ["IX509AttributeCspProvider interface [Security]","ProviderName property","IX509AttributeCspProvider.ProviderName","IX509AttributeCspProvider.get_ProviderName","IX509AttributeCspProvider::ProviderName","IX509AttributeCspProvider::get_ProviderName","ProviderName property [Security]","ProviderName property [Security]","IX509AttributeCspProvider interface","certenroll/IX509AttributeCspProvider::ProviderName","certenroll/IX509AttributeCspProvider::get_ProviderName","get_ProviderName","security.ix509attributecspprovider_providername_property"]
old-location: security\ix509attributecspprovider_providername_property.htm
tech.root: security
ms.assetid: 4a62d1e4-4d00-416b-b44a-23a9cbc53a5b
ms.date: 12/05/2018
ms.keywords: IX509AttributeCspProvider interface [Security],ProviderName property, IX509AttributeCspProvider.ProviderName, IX509AttributeCspProvider.get_ProviderName, IX509AttributeCspProvider::ProviderName, IX509AttributeCspProvider::get_ProviderName, ProviderName property [Security], ProviderName property [Security],IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::ProviderName, certenroll/IX509AttributeCspProvider::get_ProviderName, get_ProviderName, security.ix509attributecspprovider_providername_property
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
 - IX509AttributeCspProvider::get_ProviderName
 - certenroll/IX509AttributeCspProvider::get_ProviderName
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
 - IX509AttributeCspProvider.ProviderName
 - IX509AttributeCspProvider.get_ProviderName
---

# IX509AttributeCspProvider::get_ProviderName


## -description

The <b>ProviderName</b> property retrieves the provider name.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-initializeencode">InitializeEncode</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-initializedecode">InitializeDecode</a> method to initialize the <b>ProviderName</b> property. You can also call the following properties to retrieve raw data:

<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_keyspec">KeySpec</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributecspprovider-get_signature">Signature</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributecspprovider">IX509AttributeCspProvider</a>