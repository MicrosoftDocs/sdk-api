---
UID: NF:certenroll.IX509ExtensionSubjectKeyIdentifier.get_SubjectKeyIdentifier
title: IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier (certenroll.h)
description: Retrieves a byte array that contains the key identifier.
helpviewer_keywords: ["IX509ExtensionSubjectKeyIdentifier interface [Security]","SubjectKeyIdentifier property","IX509ExtensionSubjectKeyIdentifier.SubjectKeyIdentifier","IX509ExtensionSubjectKeyIdentifier.get_SubjectKeyIdentifier","IX509ExtensionSubjectKeyIdentifier::SubjectKeyIdentifier","IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier","SubjectKeyIdentifier property [Security]","SubjectKeyIdentifier property [Security]","IX509ExtensionSubjectKeyIdentifier interface","certenroll/IX509ExtensionSubjectKeyIdentifier::SubjectKeyIdentifier","certenroll/IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier","get_SubjectKeyIdentifier","security.ix509extensionsubjectkeyidentifier_subjectkeyidentifier_property"]
old-location: security\ix509extensionsubjectkeyidentifier_subjectkeyidentifier_property.htm
tech.root: security
ms.assetid: b055197c-d659-4b92-92b2-b7955beac08a
ms.date: 12/05/2018
ms.keywords: IX509ExtensionSubjectKeyIdentifier interface [Security],SubjectKeyIdentifier property, IX509ExtensionSubjectKeyIdentifier.SubjectKeyIdentifier, IX509ExtensionSubjectKeyIdentifier.get_SubjectKeyIdentifier, IX509ExtensionSubjectKeyIdentifier::SubjectKeyIdentifier, IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier, SubjectKeyIdentifier property [Security], SubjectKeyIdentifier property [Security],IX509ExtensionSubjectKeyIdentifier interface, certenroll/IX509ExtensionSubjectKeyIdentifier::SubjectKeyIdentifier, certenroll/IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier, get_SubjectKeyIdentifier, security.ix509extensionsubjectkeyidentifier_subjectkeyidentifier_property
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
 - IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier
 - certenroll/IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier
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
 - IX509ExtensionSubjectKeyIdentifier.SubjectKeyIdentifier
 - IX509ExtensionSubjectKeyIdentifier.get_SubjectKeyIdentifier
---

# IX509ExtensionSubjectKeyIdentifier::get_SubjectKeyIdentifier


## -description

The <b>SubjectKeyIdentifier</b> property retrieves a byte array that contains the key identifier. The byte array is represented by a Unicode-encoded string.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializedecode">InitializeDecode</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionsubjectkeyidentifier-initializeencode">InitializeEncode</a> method to initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsubjectkeyidentifier">IX509ExtensionSubjectKeyIdentifier</a> object. You can also call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property to retrieve the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) associated with the extension.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsubjectkeyidentifier">IX509ExtensionSubjectKeyIdentifier</a>