---
UID: NF:certenroll.IX509PrivateKey.get_KeySpec
title: IX509PrivateKey::get_KeySpec
author: windows-sdk-content
description: Specifies or retrieves a value that identifies whether a private key can be used for signing, or encryption, or both.
old-location: security\ix509privatekey_keyspec_property.htm
old-project: seccertenroll
ms.assetid: 163e0fb5-e5b1-48db-a90f-66984530f92f
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IX509PrivateKey interface [Security],KeySpec property, IX509PrivateKey.KeySpec, IX509PrivateKey.get_KeySpec, IX509PrivateKey::KeySpec, IX509PrivateKey::get_KeySpec, IX509PrivateKey::put_KeySpec, KeySpec property [Security], KeySpec property [Security],IX509PrivateKey interface, XCN_AT_KEYEXCHANGE, XCN_AT_NONE, XCN_AT_SIGNATURE, certenroll/IX509PrivateKey::KeySpec, certenroll/IX509PrivateKey::get_KeySpec, certenroll/IX509PrivateKey::put_KeySpec, get_KeySpec, security.ix509privatekey_keyspec_property
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PrivateKey.KeySpec
 - IX509PrivateKey.get_KeySpec
 - IX509PrivateKey.put_KeySpec
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PrivateKey::get_KeySpec


## -description


The <b>KeySpec</b> property specifies or retrieves a value that identifies whether a private key can be used for signing, or encryption, or both. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



If you specify a value of XCN_AT_SIGNATURE, the <b>KeySpec</b> property automatically sets the <a href="https://msdn.microsoft.com/e983c95b-6b3a-4e27-8a23-ef9051b11a16">KeyUsage</a> property to XCN_NCRYPT_ALLOW_SIGNING_FLAG. If you specify XCN_AT_KEYEXCHANGE, the <b>KeyUsage</b> property is set to XCN_NCRYPT_ALLOW_DECRYPT_FLAG |
				 XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG. The <b>KeySpec</b> property only applies to [legacy] providers created by using CryptoAPI.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

