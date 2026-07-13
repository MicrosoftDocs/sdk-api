---
UID: NS:wincrypt._CRYPT_PKCS12_PBE_PARAMS
title: CRYPT_PKCS12_PBE_PARAMS (wincrypt.h)
description: Contains parameters used to create an encryption key, initialization vector (IV), or Message Authentication Code (MAC) key for a PKCS
helpviewer_keywords: ["CRYPT_PKCS12_PBE_PARAMS","CRYPT_PKCS12_PBE_PARAMS structure [Security]","security.crypt_pkcs12_pbe_params","wincrypt/CRYPT_PKCS12_PBE_PARAMS"]
old-location: security\crypt_pkcs12_pbe_params.htm
tech.root: security
ms.assetid: 8923bb7f-b26a-4ffc-98a3-3ae74e941329
ms.date: 12/05/2018
ms.keywords: CRYPT_PKCS12_PBE_PARAMS, CRYPT_PKCS12_PBE_PARAMS structure [Security], security.crypt_pkcs12_pbe_params, wincrypt/CRYPT_PKCS12_PBE_PARAMS
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
targetos: Windows
req.typenames: CRYPT_PKCS12_PBE_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PKCS12_PBE_PARAMS
 - wincrypt/_CRYPT_PKCS12_PBE_PARAMS
 - CRYPT_PKCS12_PBE_PARAMS
 - wincrypt/CRYPT_PKCS12_PBE_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_PKCS12_PBE_PARAMS
---

# CRYPT_PKCS12_PBE_PARAMS structure


## -description

The <b>CRYPT_PKCS12_PBE_PARAMS</b> structure contains parameters used to create an encryption key, <a href="/windows/desktop/SecGloss/i-gly">initialization vector</a> (IV), or <a href="/windows/desktop/SecGloss/m-gly">Message Authentication Code</a> (MAC) key for a <a href="/windows/desktop/SecGloss/p-gly">PKCS #12</a> password based encryption algorithm.

## -struct-fields

### -field iIterations

An integer that specifies the number of hashes of the password and salt that are used to create the key.

### -field cbSalt

An integer that specifies the size, in bytes, of the salt used to create the key.

## -remarks

The buffer that contains the salt immediately follows the <b>CRYPT_PKCS12_PBE_PARAMS</b> structure.

The <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptexportkey">NCryptExportKey</a> and <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptimportkey">NCryptImportKey</a> functions consume the <b>CRYPT_PKCS12_PBE_PARAMS</b> structure as an <a href="/windows/win32/api/bcrypt/ns-bcrypt-bcryptbuffer">NCryptBuffer</a> structure in the <i>pParameterList</i> parameter.

The <a href="/windows/desktop/SecGloss/p-gly">PKCS #12</a> standard recommends a value of 1024 or greater for the <b>iIterations</b> member.