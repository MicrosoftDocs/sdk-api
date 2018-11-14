---
UID: NF:certenroll.IX509ExtensionAuthorityKeyIdentifier.get_AuthorityKeyIdentifier
title: IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier
author: windows-sdk-content
description: Retrieves a byte array that contains the extension value.
old-location: security\ix509extensionauthoritykeyidentifier_authoritykeyidentifier_property.htm
tech.root: SecCertEnroll
ms.assetid: 6ebb3f2f-c7ec-4898-a47b-681d510a7c6d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AuthorityKeyIdentifier property [Security], AuthorityKeyIdentifier property [Security],IX509ExtensionAuthorityKeyIdentifier interface, IX509ExtensionAuthorityKeyIdentifier interface [Security],AuthorityKeyIdentifier property, IX509ExtensionAuthorityKeyIdentifier.AuthorityKeyIdentifier, IX509ExtensionAuthorityKeyIdentifier.get_AuthorityKeyIdentifier, IX509ExtensionAuthorityKeyIdentifier::AuthorityKeyIdentifier, IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier, certenroll/IX509ExtensionAuthorityKeyIdentifier::AuthorityKeyIdentifier, certenroll/IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier, get_AuthorityKeyIdentifier, security.ix509extensionauthoritykeyidentifier_authoritykeyidentifier_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509ExtensionAuthorityKeyIdentifier.get_AuthorityKeyIdentifier
: 
---

# IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier


## -description


The <b>AuthorityKeyIdentifier</b> property retrieves a byte array  that contains the extension value. The byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/ce37bcba-05b1-4d42-8853-14fecbcb436b">InitializeDecode</a> method or the <a href="https://msdn.microsoft.com/450e65f9-cca0-42bd-b70b-baaf2e353812">InitializeEncode</a> method to initialize the <a href="https://msdn.microsoft.com/68889c3e-25ea-440a-a776-ef3d11dc6b54">IX509ExtensionAuthorityKeyIdentifier</a> object.  You can also call the <a href="https://msdn.microsoft.com/b03ec7fe-78e9-4a8a-81b8-eaa91aa8d072">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/68889c3e-25ea-440a-a776-ef3d11dc6b54">IX509ExtensionAuthorityKeyIdentifier</a>
 

 

