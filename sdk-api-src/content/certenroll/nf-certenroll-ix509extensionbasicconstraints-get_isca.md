---
UID: NF:certenroll.IX509ExtensionBasicConstraints.get_IsCA
title: IX509ExtensionBasicConstraints::get_IsCA (certenroll.h)
description: Retrieves a Boolean value that identifies whether the subject of the certificate is a certification authority (CA).
helpviewer_keywords: ["IX509ExtensionBasicConstraints interface [Security]","IsCA property","IX509ExtensionBasicConstraints.IsCA","IX509ExtensionBasicConstraints.get_IsCA","IX509ExtensionBasicConstraints::IsCA","IX509ExtensionBasicConstraints::get_IsCA","IsCA property [Security]","IsCA property [Security]","IX509ExtensionBasicConstraints interface","certenroll/IX509ExtensionBasicConstraints::IsCA","certenroll/IX509ExtensionBasicConstraints::get_IsCA","get_IsCA","security.ix509extensionbasicconstraints_isca_property"]
old-location: security\ix509extensionbasicconstraints_isca_property.htm
tech.root: security
ms.assetid: 1547d015-b497-4f91-acc2-4cbb2a69709f
ms.date: 12/05/2018
ms.keywords: IX509ExtensionBasicConstraints interface [Security],IsCA property, IX509ExtensionBasicConstraints.IsCA, IX509ExtensionBasicConstraints.get_IsCA, IX509ExtensionBasicConstraints::IsCA, IX509ExtensionBasicConstraints::get_IsCA, IsCA property [Security], IsCA property [Security],IX509ExtensionBasicConstraints interface, certenroll/IX509ExtensionBasicConstraints::IsCA, certenroll/IX509ExtensionBasicConstraints::get_IsCA, get_IsCA, security.ix509extensionbasicconstraints_isca_property
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
 - IX509ExtensionBasicConstraints::get_IsCA
 - certenroll/IX509ExtensionBasicConstraints::get_IsCA
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
 - IX509ExtensionBasicConstraints.IsCA
 - IX509ExtensionBasicConstraints.get_IsCA
---

# IX509ExtensionBasicConstraints::get_IsCA


## -description

The <b>IsCA</b> property retrieves a Boolean value that identifies whether the subject of the certificate is a certification authority (CA).

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-initializeencode">InitializeEncode</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionbasicconstraints-initializedecode">InitializeDecode</a> method to initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionbasicconstraints">IX509ExtensionBasicConstraints</a> object and specify the <b>IsCA</b> property. You can also call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property to retrieve the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) associated with the extension.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionbasicconstraints">IX509ExtensionBasicConstraints</a>