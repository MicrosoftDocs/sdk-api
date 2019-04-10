---
UID: NC:cryptxml.CryptXmlDllCreateKey
title: CryptXmlDllCreateKey (cryptxml.h)
author: windows-sdk-content
description: Parses the KeyValue element and creates a Cryptography API:\_Next Generation (CNG) BCrypt key handle to verify a signature.
old-location: security\cryptxmldllcreatekey.htm
tech.root: SecCrypto
ms.assetid: a2c4b4b5-ccfc-4fb9-ad03-942906cf73d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptXmlDllCreateKey, CryptXmlDllCreateKey callback, CryptXmlDllCreateKey callback function [Security], cryptxml/CryptXmlDllCreateKey, security.cryptxmldllcreatekey
ms.topic: callback
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - cryptxml.h
api_name:
 - CryptXmlDllCreateKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlDllCreateKey callback function


## -description


the <b>CryptXmlDllCreateKey</b> function parses the <b>KeyValue</b> element and creates a Cryptography API: Next Generation (CNG) BCrypt key handle to verify a signature.


## -parameters




### -param *pEncoded [in]

A pointer to a <a href="https://msdn.microsoft.com/b70aae53-919b-4d4a-b284-ea6bc223842f">CRYPT_XML_BLOB</a> structure that contains the <b>KeyValue</b> element.


### -param *phKey [out]

A pointer to a <b>BCRYPT_KEY_HANDLE</b> variable that receives the handle of the key used to verify the signature.

When CryptXML has finished using the key, CryptXML frees it by calling the <a href="https://msdn.microsoft.com/98c02e55-6489-4901-8a7a-021baac41965">BCryptDestroyKey</a> function.


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



