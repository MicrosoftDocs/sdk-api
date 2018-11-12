---
UID: NS:wincrypt._CRYPT_PKCS12_PBE_PARAMS
title: "_CRYPT_PKCS12_PBE_PARAMS"
author: windows-sdk-content
description: Contains parameters used to create an encryption key, initialization vector (IV), or Message Authentication Code (MAC) key for a PKCS #12 password based encryption algorithm.
old-location: security\crypt_pkcs12_pbe_params.htm
tech.root: seccrypto
ms.assetid: 8923bb7f-b26a-4ffc-98a3-3ae74e941329
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CRYPT_PKCS12_PBE_PARAMS, CRYPT_PKCS12_PBE_PARAMS structure [Security], _CRYPT_PKCS12_PBE_PARAMS, security.crypt_pkcs12_pbe_params, wincrypt/CRYPT_PKCS12_PBE_PARAMS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_PKCS12_PBE_PARAMS
product: Windows
targetos: Windows
req.typenames: CRYPT_PKCS12_PBE_PARAMS
req.redist: 
---

# _CRYPT_PKCS12_PBE_PARAMS structure


## -description


The <b>CRYPT_PKCS12_PBE_PARAMS</b> structure contains parameters used to create an encryption key, <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">initialization vector</a> (IV), or <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Message Authentication Code</a> (MAC) key for a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #12</a> password based encryption algorithm.


## -struct-fields




### -field iIterations

An integer that specifies the number of hashes of the password and salt that are used to create the key.


### -field cbSalt

An integer that specifies the size, in bytes, of the salt used to create the key.


## -remarks



The buffer that contains the salt immediately follows the <b>CRYPT_PKCS12_PBE_PARAMS</b> structure.

The <a href="https://msdn.microsoft.com/1588eb29-4026-4d1c-8bee-a035df38444a">NCryptExportKey</a> and <a href="https://msdn.microsoft.com/ede0e7e0-cb2c-44c0-b724-58db3480b781">NCryptImportKey</a> functions consume the <b>CRYPT_PKCS12_PBE_PARAMS</b> structure as an <a href="https://msdn.microsoft.com/474d3c0d-ae14-448a-a56d-25abc7e5de88">NCryptBuffer</a> structure in the <i>pParameterList</i> parameter.

The <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">PKCS #12</a> standard recommends a value of 1024 or greater for the <b>iIterations</b> member.



