---
UID: NS:wincrypt._CRYPT_PASSWORD_CREDENTIALSA
title: CRYPT_PASSWORD_CREDENTIALSA (wincrypt.h)
description: Contains the user name and password credentials to be used in the CRYPT_CREDENTIALS structure as optional input to a remote object retrieval function such as CryptRetrieveObjectByUrl or CryptGetTimeValidObject. (ANSI)
helpviewer_keywords: ["*PCRYPT_PASSWORD_CREDENTIALSA","CRYPT_PASSWORD_CREDENTIALS","CRYPT_PASSWORD_CREDENTIALS structure [Security]","CRYPT_PASSWORD_CREDENTIALSA","CRYPT_PASSWORD_CREDENTIALSW","PCRYPT_PASSWORD_CREDENTIALS","PCRYPT_PASSWORD_CREDENTIALS structure pointer [Security]","security.crypt_password_credentials","wincrypt/CRYPT_PASSWORD_CREDENTIALS","wincrypt/CRYPT_PASSWORD_CREDENTIALSA","wincrypt/CRYPT_PASSWORD_CREDENTIALSW","wincrypt/PCRYPT_PASSWORD_CREDENTIALS"]
old-location: security\crypt_password_credentials.htm
tech.root: security
ms.assetid: 21461344-1080-4603-bda1-a92dfda68c15
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PASSWORD_CREDENTIALSA, CRYPT_PASSWORD_CREDENTIALS, CRYPT_PASSWORD_CREDENTIALS structure [Security], CRYPT_PASSWORD_CREDENTIALSA, CRYPT_PASSWORD_CREDENTIALSW, PCRYPT_PASSWORD_CREDENTIALS, PCRYPT_PASSWORD_CREDENTIALS structure pointer [Security], security.crypt_password_credentials, wincrypt/CRYPT_PASSWORD_CREDENTIALS, wincrypt/CRYPT_PASSWORD_CREDENTIALSA, wincrypt/CRYPT_PASSWORD_CREDENTIALSW, wincrypt/PCRYPT_PASSWORD_CREDENTIALS'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CRYPT_PASSWORD_CREDENTIALSW (Unicode) and CRYPT_PASSWORD_CREDENTIALSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPT_PASSWORD_CREDENTIALSA, *PCRYPT_PASSWORD_CREDENTIALSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PASSWORD_CREDENTIALSA
 - wincrypt/_CRYPT_PASSWORD_CREDENTIALSA
 - PCRYPT_PASSWORD_CREDENTIALSA
 - wincrypt/PCRYPT_PASSWORD_CREDENTIALSA
 - CRYPT_PASSWORD_CREDENTIALSA
 - wincrypt/CRYPT_PASSWORD_CREDENTIALSA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinCrypt.h
api_name:
 - CRYPT_PASSWORD_CREDENTIALS
 - CRYPT_PASSWORD_CREDENTIALSA
 - CRYPT_PASSWORD_CREDENTIALSW
---

# CRYPT_PASSWORD_CREDENTIALSA structure


## -description

The <b>CRYPT_PASSWORD_CREDENTIALS</b> structure contains the user name and password credentials to be used in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_credentials">CRYPT_CREDENTIALS</a> structure as optional input to a remote object retrieval function such as <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptretrieveobjectbyurla">CryptRetrieveObjectByUrl</a> or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgettimevalidobject">CryptGetTimeValidObject</a>.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field pszUsername

A pointer to a null-terminated string that contains the user name credential for the remote session authentication.

### -field pszPassword

A pointer to a null-terminated string that contains the password credential for the remote session authentication.

## -remarks

> [!NOTE]
> The wincrypt.h header defines CRYPT_PASSWORD_CREDENTIALS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
