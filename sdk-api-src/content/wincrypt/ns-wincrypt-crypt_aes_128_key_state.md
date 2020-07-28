---
UID: NS:wincrypt._CRYPT_AES_128_KEY_STATE
title: CRYPT_AES_128_KEY_STATE (wincrypt.h)
description: Specifies the 128-bit symmetric key information for an Advanced Encryption Standard (AES) cipher.
helpviewer_keywords: ["*PCRYPT_AES_128_KEY_STATE","CRYPT_AES_128_KEY_STATE","CRYPT_AES_128_KEY_STATE structure [Security]","PCRYPT_AES_128_KEY_STATE","PCRYPT_AES_128_KEY_STATE structure pointer [Security]","security.crypt_aes_128_key_state","wincrypt/CRYPT_AES_128_KEY_STATE","wincrypt/PCRYPT_AES_128_KEY_STATE"]
old-location: security\crypt_aes_128_key_state.htm
tech.root: security
ms.assetid: 1a472caa-e57a-4b3a-ab28-8aacf8e39ad1
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_AES_128_KEY_STATE, CRYPT_AES_128_KEY_STATE, CRYPT_AES_128_KEY_STATE structure [Security], PCRYPT_AES_128_KEY_STATE, PCRYPT_AES_128_KEY_STATE structure pointer [Security], security.crypt_aes_128_key_state, wincrypt/CRYPT_AES_128_KEY_STATE, wincrypt/PCRYPT_AES_128_KEY_STATE'
f1_keywords:
- wincrypt/CRYPT_AES_128_KEY_STATE
dev_langs:
- c++
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
targetos: Windows
req.typenames: CRYPT_AES_128_KEY_STATE, *PCRYPT_AES_128_KEY_STATE
req.redist: 
ms.custom: 19H1
---

# CRYPT_AES_128_KEY_STATE structure


## -description


The <b>CRYPT_AES_128_KEY_STATE</b> structure specifies the 128-bit <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">symmetric key</a> information for an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Advanced Encryption Standard</a> (AES) cipher.


## -struct-fields




### -field Key

An array of hexadecimal values that specify a 128-bit <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cipher</a> key.


### -field IV

An array of hexadecimal values that specify an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/i-gly">initialization vector</a> (IV) for the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cipher</a>.


### -field EncryptionState

An array of hexadecimal values that specify an 11-round encryption key schedule.


### -field DecryptionState

An array of hexadecimal values that specify an 11-round decryption key schedule.


### -field Feedback

An array of hexadecimal values that specify the feedback vector for a stage in the encryption or decryption process.


## -remarks



The <b>CRYPT_AES_128_KEY_STATE</b> structure is used by the <a href="https://docs.microsoft.com/previous-versions/aa379853(v=vs.85)">CPImportKey</a> and <a href="https://docs.microsoft.com/previous-versions/aa378203(v=vs.85)">CPExportKey</a> functions when the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">key BLOB</a> was created by using the <i>dwBlobType</i>  parameter set to the <b>KEYSTATEBLOB</b> value.

   The Microsoft AES Cryptographic Provider only supports this structure in the context of the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">Secure Sockets Layer protocol</a> (SSL), where the caller specified <b>PROV_DH_SCHANNEL</b> as the value for the <i>dwProvType</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function.



