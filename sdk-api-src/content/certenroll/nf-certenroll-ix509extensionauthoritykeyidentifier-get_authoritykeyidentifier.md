---
UID: NF:certenroll.IX509ExtensionAuthorityKeyIdentifier.get_AuthorityKeyIdentifier
title: IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier
author: windows-sdk-content
description: Retrieves a byte array that contains the extension value.
old-location: security\ix509extensionauthoritykeyidentifier_authoritykeyidentifier_property.htm
tech.root: SecCertEnroll
ms.assetid: 6ebb3f2f-c7ec-4898-a47b-681d510a7c6d
ms.author: windowssdkdev
ms.date: 08/29/2018
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
---

# IX509ExtensionAuthorityKeyIdentifier::get_AuthorityKeyIdentifier


## -description


The <b>AuthorityKeyIdentifier</b> property retrieves a byte array  that contains the extension value. The byte array is represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378101(v=VS.85).aspx">InitializeDecode</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa378103(v=VS.85).aspx">InitializeEncode</a> method to initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa378098(v=VS.85).aspx">IX509ExtensionAuthorityKeyIdentifier</a> object.  You can also call the <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378098(v=VS.85).aspx">IX509ExtensionAuthorityKeyIdentifier</a>
 

 

