---
UID: NS:bcrypt._BCRYPT_PKCS1_PADDING_INFO
title: BCRYPT_PKCS1_PADDING_INFO (bcrypt.h)
description: Used to provide options for the PKCS
helpviewer_keywords: ["BCRYPT_PKCS1_PADDING_INFO","BCRYPT_PKCS1_PADDING_INFO structure [Security]","bcrypt/BCRYPT_PKCS1_PADDING_INFO","security.bcrypt_pkcs1_padding_info"]
old-location: security\bcrypt_pkcs1_padding_info.htm
tech.root: security
ms.assetid: 920fa461-5b7e-4429-972d-e7c83fb62c64
ms.date: 02/14/2024
ms.keywords: BCRYPT_PKCS1_PADDING_INFO, BCRYPT_PKCS1_PADDING_INFO structure [Security], bcrypt/BCRYPT_PKCS1_PADDING_INFO, security.bcrypt_pkcs1_padding_info
req.header: bcrypt.h
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
req.typenames: BCRYPT_PKCS1_PADDING_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_PKCS1_PADDING_INFO
 - bcrypt/_BCRYPT_PKCS1_PADDING_INFO
 - BCRYPT_PKCS1_PADDING_INFO
 - bcrypt/BCRYPT_PKCS1_PADDING_INFO
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
 - BCRYPT_PKCS1_PADDING_INFO
---

# BCRYPT_PKCS1_PADDING_INFO structure

## -description

The **BCRYPT_PKCS1_PADDING_INFO** structure is used to provide options for the [PKCS #1](/windows/win32/SecGloss/p-gly) padding scheme.

## -struct-fields

### -field pszAlgId

A pointer to a null-terminated Unicode string that identifies the [cryptographic algorithm](/windows/win32/SecGloss/c-gly) to use to create the padding. This algorithm must be a [hashing algorithm](/windows/win32/SecGloss/h-gly). When creating a signature, the [object identifier](/windows/win32/SecGloss/o-gly) (OID) that corresponds to this algorithm is added to the **DigestInfo** element in the signature, and if this member is `NULL`, then the OID is not added. When verifying a signature, the verification fails if the OID that corresponds to this member is not the same as the OID in the signature. If there is no OID in the signature, then verification fails unless this member is `NULL`.

## -see-also

[CNG Algorithm Identifiers](/windows/win32/seccng/cng-algorithm-identifiers)

[BCryptDecrypt](nf-bcrypt-bcryptdecrypt.md)

[BCryptEncrypt](nf-bcrypt-bcryptencrypt.md)

[BCryptSignHash](nf-bcrypt-bcryptsignhash.md)

[BCryptVerifySignature](nf-bcrypt-bcryptverifysignature.md)
