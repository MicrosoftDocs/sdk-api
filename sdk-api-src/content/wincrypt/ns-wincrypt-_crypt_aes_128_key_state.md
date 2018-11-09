---
UID: NS:wincrypt._CRYPT_AES_128_KEY_STATE
title: "_CRYPT_AES_128_KEY_STATE"
author: windows-sdk-content
description: Specifies the 128-bit symmetric key information for an Advanced Encryption Standard (AES) cipher.
old-location: security\crypt_aes_128_key_state.htm
tech.root: seccrypto
ms.assetid: 1a472caa-e57a-4b3a-ab28-8aacf8e39ad1
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PCRYPT_AES_128_KEY_STATE, CRYPT_AES_128_KEY_STATE, CRYPT_AES_128_KEY_STATE structure [Security], PCRYPT_AES_128_KEY_STATE, PCRYPT_AES_128_KEY_STATE structure pointer [Security], _CRYPT_AES_128_KEY_STATE, security.crypt_aes_128_key_state, wincrypt/CRYPT_AES_128_KEY_STATE, wincrypt/PCRYPT_AES_128_KEY_STATE"
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
 - CRYPT_AES_128_KEY_STATE
product: Windows
targetos: Windows
req.typenames: CRYPT_AES_128_KEY_STATE, *PCRYPT_AES_128_KEY_STATE
req.redist: 
---

# _CRYPT_AES_128_KEY_STATE structure


## -description


The <b>CRYPT_AES_128_KEY_STATE</b> structure specifies the 128-bit <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric key</a> information for an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Advanced Encryption Standard</a> (AES) cipher.


## -struct-fields




### -field Key

An array of hexadecimal values that specify a 128-bit <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cipher</a> key.


### -field IV

An array of hexadecimal values that specify an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">initialization vector</a> (IV) for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cipher</a>.


### -field EncryptionState

An array of hexadecimal values that specify an 11-round encryption key schedule.


### -field DecryptionState

An array of hexadecimal values that specify an 11-round decryption key schedule.


### -field Feedback

An array of hexadecimal values that specify the feedback vector for a stage in the encryption or decryption process.


## -remarks



The <b>CRYPT_AES_128_KEY_STATE</b> structure is used by the <a href="https://msdn.microsoft.com/5be2a327-61d1-45f6-99ee-45a2f3c4d1f8">CPImportKey</a> and <a href="https://msdn.microsoft.com/6b5114ca-2ec4-4297-9c62-60c2fd623f63">CPExportKey</a> functions when the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key BLOB</a> was created by using the <i>dwBlobType</i>  parameter set to the <b>KEYSTATEBLOB</b> value.

   The Microsoft AES Cryptographic Provider only supports this structure in the context of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Secure Sockets Layer protocol</a> (SSL), where the caller specified <b>PROV_DH_SCHANNEL</b> as the value for the <i>dwProvType</i> parameter of the <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> function.



