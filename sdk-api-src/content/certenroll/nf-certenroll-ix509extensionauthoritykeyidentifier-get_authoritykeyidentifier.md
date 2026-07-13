---
UID: NF:certenroll.IX509ExtensionAuthorityKeyIdentifier.get_AuthorityKeyIdentifier
title: IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier (certenroll.h)
description: Retrieves a byte array that contains the extension value. (IX509ExtensionAuthorityKeyIdentifier.get_AuthorityKeyIdentifier)
helpviewer_keywords: ["AuthorityKeyIdentifier property [Security]","AuthorityKeyIdentifier property [Security]","IX509ExtensionAuthorityKeyIdentifier interface","IX509ExtensionAuthorityKeyIdentifier interface [Security]","AuthorityKeyIdentifier property","IX509ExtensionAuthorityKeyIdentifier.AuthorityKeyIdentifier","IX509ExtensionAuthorityKeyIdentifier.get_AuthorityKeyIdentifier","IX509ExtensionAuthorityKeyIdentifier::AuthorityKeyIdentifier","IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier","certenroll/IX509ExtensionAuthorityKeyIdentifier::AuthorityKeyIdentifier","certenroll/IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier","get_AuthorityKeyIdentifier","security.ix509extensionauthoritykeyidentifier_authoritykeyidentifier_property"]
old-location: security\ix509extensionauthoritykeyidentifier_authoritykeyidentifier_property.htm
tech.root: security
ms.assetid: 6ebb3f2f-c7ec-4898-a47b-681d510a7c6d
ms.date: 12/05/2018
ms.keywords: AuthorityKeyIdentifier property [Security], AuthorityKeyIdentifier property [Security],IX509ExtensionAuthorityKeyIdentifier interface, IX509ExtensionAuthorityKeyIdentifier interface [Security],AuthorityKeyIdentifier property, IX509ExtensionAuthorityKeyIdentifier.AuthorityKeyIdentifier, IX509ExtensionAuthorityKeyIdentifier.get_AuthorityKeyIdentifier, IX509ExtensionAuthorityKeyIdentifier::AuthorityKeyIdentifier, IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier, certenroll/IX509ExtensionAuthorityKeyIdentifier::AuthorityKeyIdentifier, certenroll/IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier, get_AuthorityKeyIdentifier, security.ix509extensionauthoritykeyidentifier_authoritykeyidentifier_property
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
 - IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier
 - certenroll/IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier
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
 - IX509ExtensionAuthorityKeyIdentifier.AuthorityKeyIdentifier
 - IX509ExtensionAuthorityKeyIdentifier.get_AuthorityKeyIdentifier
---

# IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier


## -description

The <b>AuthorityKeyIdentifier</b> property retrieves a byte array  that contains the extension value. The byte array is represented by a Unicode-encoded string.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionauthoritykeyidentifier-initializedecode">InitializeDecode</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionauthoritykeyidentifier-initializeencode">InitializeEncode</a> method to initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionauthoritykeyidentifier">IX509ExtensionAuthorityKeyIdentifier</a> object.  You can also call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property to retrieve the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) associated with the extension.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionauthoritykeyidentifier">IX509ExtensionAuthorityKeyIdentifier</a>
