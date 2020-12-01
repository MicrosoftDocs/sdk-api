---
UID: NS:wincrypt._CRYPT_DECODE_PARA
title: CRYPT_DECODE_PARA (wincrypt.h)
description: Used by the CryptDecodeObjectEx function to provide access to memory allocation and memory freeing callback functions.
helpviewer_keywords: ["*PCRYPT_DECODE_PARA","CRYPT_DECODE_PARA","CRYPT_DECODE_PARA structure [Security]","PCRYPT_DECODE_PARA","PCRYPT_DECODE_PARA structure pointer [Security]","security.crypt_decode_para","wincrypt/CRYPT_DECODE_PARA","wincrypt/PCRYPT_DECODE_PARA"]
old-location: security\crypt_decode_para.htm
tech.root: security
ms.assetid: 08ed4627-8cbf-415f-b0d0-2c4b9ed9aed1
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_DECODE_PARA, CRYPT_DECODE_PARA, CRYPT_DECODE_PARA structure [Security], PCRYPT_DECODE_PARA, PCRYPT_DECODE_PARA structure pointer [Security], security.crypt_decode_para, wincrypt/CRYPT_DECODE_PARA, wincrypt/PCRYPT_DECODE_PARA'
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
req.typenames: CRYPT_DECODE_PARA, *PCRYPT_DECODE_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_DECODE_PARA
 - wincrypt/_CRYPT_DECODE_PARA
 - PCRYPT_DECODE_PARA
 - wincrypt/PCRYPT_DECODE_PARA
 - CRYPT_DECODE_PARA
 - wincrypt/CRYPT_DECODE_PARA
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
 - CRYPT_DECODE_PARA
---

# CRYPT_DECODE_PARA structure


## -description

The <b>CRYPT_DECODE_PARA</b> structure is used by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobjectex">CryptDecodeObjectEx</a> function to provide access to memory allocation and memory freeing callback functions.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field pfnAlloc

This member is an optional pointer to a callback function used to allocate memory.

### -field pfnFree

This member is an optional pointer to a callback function used to free memory allocated by the allocate callback function.