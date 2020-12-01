---
UID: NS:wincrypt._CRYPT_ENCODE_PARA
title: CRYPT_ENCODE_PARA (wincrypt.h)
description: Used by the CryptEncodeObjectEx function to provide access to memory allocation and memory freeing callback functions.
helpviewer_keywords: ["*PCRYPT_ENCODE_PARA","CRYPT_ENCODE_PARA","CRYPT_ENCODE_PARA structure [Security]","PCRYPT_ENCODE_PARA","PCRYPT_ENCODE_PARA structure pointer [Security]","_crypto2_crypt_encode_para","security.crypt_encode_para","wincrypt/CRYPT_ENCODE_PARA","wincrypt/PCRYPT_ENCODE_PARA"]
old-location: security\crypt_encode_para.htm
tech.root: security
ms.assetid: 330af6ac-f1db-4cee-81fd-d3c2c341d493
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_ENCODE_PARA, CRYPT_ENCODE_PARA, CRYPT_ENCODE_PARA structure [Security], PCRYPT_ENCODE_PARA, PCRYPT_ENCODE_PARA structure pointer [Security], _crypto2_crypt_encode_para, security.crypt_encode_para, wincrypt/CRYPT_ENCODE_PARA, wincrypt/PCRYPT_ENCODE_PARA'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CRYPT_ENCODE_PARA, *PCRYPT_ENCODE_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_ENCODE_PARA
 - wincrypt/_CRYPT_ENCODE_PARA
 - PCRYPT_ENCODE_PARA
 - wincrypt/PCRYPT_ENCODE_PARA
 - CRYPT_ENCODE_PARA
 - wincrypt/CRYPT_ENCODE_PARA
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
 - CRYPT_ENCODE_PARA
---

# CRYPT_ENCODE_PARA structure


## -description

The <b>CRYPT_ENCODE_PARA</b> structure is used by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobjectex">CryptEncodeObjectEx</a> function to provide access to memory allocation and memory freeing callback functions.

## -struct-fields

### -field cbSize

Indicates the size, in bytes, of the structure.

### -field pfnAlloc

This member is an optional pointer to a callback function used to allocate memory.

### -field pfnFree

This member is an optional pointer to a callback function used to free memory allocated by the allocate callback function.