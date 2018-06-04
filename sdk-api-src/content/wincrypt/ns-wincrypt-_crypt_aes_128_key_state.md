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



