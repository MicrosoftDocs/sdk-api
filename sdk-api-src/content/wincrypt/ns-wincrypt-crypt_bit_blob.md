---
UID: NS:wincrypt._CRYPT_BIT_BLOB
title: CRYPT_BIT_BLOB (wincrypt.h)
description: Contains a set of bits represented by an array of bytes.
helpviewer_keywords: ["*PCRYPT_BIT_BLOB","CRYPT_BIT_BLOB","CRYPT_BIT_BLOB structure [Security]","PCRYPT_BIT_BLOB","PCRYPT_BIT_BLOB structure pointer [Security]","_crypto2_crypt_bit_blob","security.crypt_bit_blob","wincrypt/CRYPT_BIT_BLOB","wincrypt/PCRYPT_BIT_BLOB"]
old-location: security\crypt_bit_blob.htm
tech.root: security
ms.assetid: 6f102ff3-bfff-4415-a5d8-ca2c226074b3
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_BIT_BLOB, CRYPT_BIT_BLOB, CRYPT_BIT_BLOB structure [Security], PCRYPT_BIT_BLOB, PCRYPT_BIT_BLOB structure pointer [Security], _crypto2_crypt_bit_blob, security.crypt_bit_blob, wincrypt/CRYPT_BIT_BLOB, wincrypt/PCRYPT_BIT_BLOB'
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
req.typenames: CRYPT_BIT_BLOB, *PCRYPT_BIT_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_BIT_BLOB
 - wincrypt/_CRYPT_BIT_BLOB
 - PCRYPT_BIT_BLOB
 - wincrypt/PCRYPT_BIT_BLOB
 - CRYPT_BIT_BLOB
 - wincrypt/CRYPT_BIT_BLOB
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
 - CRYPT_BIT_BLOB
---

# CRYPT_BIT_BLOB structure


## -description

The <b>CRYPT_BIT_BLOB</b> structure contains a set of bits represented by an array of bytes.

## -struct-fields

### -field cbData

The number of bytes in the <b>pbData</b> array.

### -field pbData

A pointer to an array of bytes that represents the bits.

### -field cUnusedBits

The number of unused bits in the last byte of the array. The unused bits are always the least significant bits in the last byte of the array.

## -remarks

Because the smallest chunk of memory that can normally be allocated is a byte, the <b>CRYPT_BIT_BLOB</b> structure allows the last byte in the array to contain zero to seven unused bits. The number of unused bits in the array is contained  in the <b>cUnusedBits</b> member of this structure. The number of meaningful bits in the <b>pbData</b> member is calculated with the formula ((<b>cbData</b> × 8) –<b>cUnusedBits</b>). For example, if you need to represent 10 bits, you would allocate an array of 2 bytes and set <b>cUnusedBits</b> to 6. If you view the array as contiguous bits from left to right, the left 10 bits would be meaningful, and the right 6 bits would be unused.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_basic_constraints_info">CERT_BASIC_CONSTRAINTS_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_attributes_info">CERT_KEY_ATTRIBUTES_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_usage_restriction_info">CERT_KEY_USAGE_RESTRICTION_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_signed_content_info">CERT_SIGNED_CONTENT_INFO</a>