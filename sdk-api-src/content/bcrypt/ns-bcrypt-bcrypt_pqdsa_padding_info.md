---
UID: NS:bcrypt._BCRYPT_PQDSA_PADDING_INFO
title: BCRYPT_PQDSA_PADDING_INFO (bcrypt.h)
description: Used to specify the padding scheme for post-quantum digital signature algorithms.
helpviewer_keywords: ["BCRYPT_PQDSA_PADDING_INFO","BCRYPT_PQDSA_PADDING_INFO structure [Security]","bcrypt/BCRYPT_PQDSA_PADDING_INFO","security.bcrypt_pqdsa_padding_info"]
old-location: 
tech.root: security
ms.assetid: 
ms.date: 05/26/2026
ms.keywords: BCRYPT_PQDSA_PADDING_INFO, BCRYPT_PQDSA_PADDING_INFO structure [Security], bcrypt/BCRYPT_PQDSA_PADDING_INFO, security.bcrypt_pqdsa_padding_info
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 11 24H2
req.target-min-winversvr: Windows Server 2025
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
req.typenames: BCRYPT_PQDSA_PADDING_INFO
req.redist: 
ms.custom: 24H2
f1_keywords:
 - _BCRYPT_PQDSA_PADDING_INFO
 - bcrypt/_BCRYPT_PQDSA_PADDING_INFO
 - BCRYPT_PQDSA_PADDING_INFO
 - bcrypt/BCRYPT_PQDSA_PADDING_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_PQDSA_PADDING_INFO
---

# BCRYPT_PQDSA_PADDING_INFO structure

> [!NOTE]
> Some information relates to a prerelease product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here. The feature described in this topic is available in pre-release versions of the [Windows Insider Preview](https://www.microsoft.com/software-download/windowsinsiderpreviewSDK).

## -description

The **BCRYPT_PQDSA_PADDING_INFO** structure is used to specify the padding scheme for Post-Quantum Digital Signature algorithms (PQDSA).

## -struct-fields

### -field pbCtx

A pointer to the buffer that contains the context string.

May be `NULL`. If **pbCtx** is `NULL`, then **cbCtx** must be set to `0`.

### -field cbCtx

The size, in bytes, of the context string pointed to by **pbCtx**. Its value must be `0` if **pbCtx** is `NULL`. Otherwise, it must be a non-zero integer less than `256`.

### -field pszPrehashAlgId

A CNG hash [algorithm identifier](/windows/win32/SecCNG/cng-algorithm-identifiers). This parameter indicates whether the pure (e.g. ML-DSA) or the pre-hash (e.g. HashML-DSA) variant will be used. A `NULL` value indicates the use of pure variant. To use a pre-hash variant, this identifier must refer to an approved hash algorithm: SHA-2, SHA-3, or SHAKE.

## Remarks

For many PQDSA signatures, the use of **BCRYPT_PQDSA_PADDING_INFO** is not required. Using `NULL` *pPaddingInfo* in calls to [BCryptSignHash](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsignhash) and [BCryptVerifySignature](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptverifysignature) is equivalent to using pure variant with an empty context string.

## -see-also

[CNG Algorithm Identifiers](/windows/win32/seccng/cng-algorithm-identifiers)

[BCryptDecrypt](nf-bcrypt-bcryptdecrypt.md)

[BCryptEncrypt](nf-bcrypt-bcryptencrypt.md)

[BCryptSignHash](nf-bcrypt-bcryptsignhash.md)

[BCryptVerifySignature](nf-bcrypt-bcryptverifysignature.md)