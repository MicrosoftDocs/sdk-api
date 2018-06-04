---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

