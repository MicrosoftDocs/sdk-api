---
UID: NF:certenroll.IX509ExtensionAlternativeNames.get_AlternativeNames
title: IX509ExtensionAlternativeNames::get_AlternativeNames (certenroll.h)
description: Retrieves a collection of subject alternative names.
helpviewer_keywords: ["AlternativeNames property [Security]","AlternativeNames property [Security]","IX509ExtensionAlternativeNames interface","IX509ExtensionAlternativeNames interface [Security]","AlternativeNames property","IX509ExtensionAlternativeNames.AlternativeNames","IX509ExtensionAlternativeNames.get_AlternativeNames","IX509ExtensionAlternativeNames::AlternativeNames","IX509ExtensionAlternativeNames::get_AlternativeNames","certenroll/IX509ExtensionAlternativeNames::AlternativeNames","certenroll/IX509ExtensionAlternativeNames::get_AlternativeNames","get_AlternativeNames","security.ix509extensionalternativenames_alternativenames_property"]
old-location: security\ix509extensionalternativenames_alternativenames_property.htm
tech.root: security
ms.assetid: 816afa9d-2283-4e17-ad12-ee53e5353d83
ms.date: 12/05/2018
ms.keywords: AlternativeNames property [Security], AlternativeNames property [Security],IX509ExtensionAlternativeNames interface, IX509ExtensionAlternativeNames interface [Security],AlternativeNames property, IX509ExtensionAlternativeNames.AlternativeNames, IX509ExtensionAlternativeNames.get_AlternativeNames, IX509ExtensionAlternativeNames::AlternativeNames, IX509ExtensionAlternativeNames::get_AlternativeNames, certenroll/IX509ExtensionAlternativeNames::AlternativeNames, certenroll/IX509ExtensionAlternativeNames::get_AlternativeNames, get_AlternativeNames, security.ix509extensionalternativenames_alternativenames_property
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
 - IX509ExtensionAlternativeNames::get_AlternativeNames
 - certenroll/IX509ExtensionAlternativeNames::get_AlternativeNames
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
 - IX509ExtensionAlternativeNames.AlternativeNames
 - IX509ExtensionAlternativeNames.get_AlternativeNames
---

# IX509ExtensionAlternativeNames::get_AlternativeNames


## -description

The <b>AlternativeNames</b> property retrieves a collection of subject alternative names.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionalternativenames-initializeencode">InitializeEncode</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionalternativenames-initializedecode">InitializeDecode</a> method to initialize the collection. You can also call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property to retrieve the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) associated with the extension.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionalternativenames">IX509ExtensionAlternativeNames</a>