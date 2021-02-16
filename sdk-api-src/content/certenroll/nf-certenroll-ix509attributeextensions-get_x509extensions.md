---
UID: NF:certenroll.IX509AttributeExtensions.get_X509Extensions
title: IX509AttributeExtensions::get_X509Extensions (certenroll.h)
description: Retrieves the certificate extensions.
helpviewer_keywords: ["IX509AttributeExtensions interface [Security]","X509Extensions property","IX509AttributeExtensions.X509Extensions","IX509AttributeExtensions.get_X509Extensions","IX509AttributeExtensions::X509Extensions","IX509AttributeExtensions::get_X509Extensions","X509Extensions property [Security]","X509Extensions property [Security]","IX509AttributeExtensions interface","certenroll/IX509AttributeExtensions::X509Extensions","certenroll/IX509AttributeExtensions::get_X509Extensions","get_X509Extensions","security.ix509attributeextensions_x509extensions_property"]
old-location: security\ix509attributeextensions_x509extensions_property.htm
tech.root: security
ms.assetid: 719c4ac5-8d67-4026-9eb6-9682942ad367
ms.date: 12/05/2018
ms.keywords: IX509AttributeExtensions interface [Security],X509Extensions property, IX509AttributeExtensions.X509Extensions, IX509AttributeExtensions.get_X509Extensions, IX509AttributeExtensions::X509Extensions, IX509AttributeExtensions::get_X509Extensions, X509Extensions property [Security], X509Extensions property [Security],IX509AttributeExtensions interface, certenroll/IX509AttributeExtensions::X509Extensions, certenroll/IX509AttributeExtensions::get_X509Extensions, get_X509Extensions, security.ix509attributeextensions_x509extensions_property
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
 - IX509AttributeExtensions::get_X509Extensions
 - certenroll/IX509AttributeExtensions::get_X509Extensions
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
 - IX509AttributeExtensions.X509Extensions
 - IX509AttributeExtensions.get_X509Extensions
---

# IX509AttributeExtensions::get_X509Extensions


## -description

The <b>X509Extensions</b> property retrieves the certificate extensions.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeextensions-initializeencode">InitializeEncode</a> method or the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509attributeextensions-initializedecode">InitializeDecode</a> method to initialize the <b>X509Extensions</b> property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>