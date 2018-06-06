---
UID: NF:certenroll.IX509PrivateKey.put_KeyUsage
title: IX509PrivateKey::put_KeyUsage
author: windows-sdk-content
description: Specifies or retrieves a value that identifies the specific purpose for which a private key can be used.
old-location: security\ix509privatekey_keyusage.htm
old-project: SecCertEnroll
ms.assetid: e983c95b-6b3a-4e27-8a23-ef9051b11a16
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509PrivateKey interface [Security],KeyUsage property, IX509PrivateKey.KeyUsage, IX509PrivateKey.put_KeyUsage, IX509PrivateKey::KeyUsage, IX509PrivateKey::get_KeyUsage, IX509PrivateKey::put_KeyUsage, KeyUsage property [Security], KeyUsage property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::KeyUsage, certenroll/IX509PrivateKey::get_KeyUsage, certenroll/IX509PrivateKey::put_KeyUsage, put_KeyUsage, security.ix509privatekey_keyusage
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
 - IX509PrivateKey.KeyUsage
 - IX509PrivateKey.get_KeyUsage
 - IX509PrivateKey.put_KeyUsage
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PrivateKey::put_KeyUsage


## -description


The <b>KeyUsage</b> property specifies or retrieves a  value that identifies the specific purpose for which a private key can be used. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



If you set the <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property for a  legacy CSP to XCN_NCRYPT_ALLOW_SIGNING_FLAG, the <b>KeyUsage</b> property to XCN_NCRYPT_ALLOW_SIGNING_FLAG. If you specify XCN_AT_KEYEXCHANGE, the <b>KeyUsage</b> property is automatically set to XCN_NCRYPT_ALLOW_DECRYPT_FLAG |
             XCN_NCRYPT_ALLOW_KEY_AGREEMENT_FLAG.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

