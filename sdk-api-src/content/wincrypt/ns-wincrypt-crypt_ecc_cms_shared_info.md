---
UID: NS:wincrypt._CRYPT_ECC_CMS_SHARED_INFO
title: CRYPT_ECC_CMS_SHARED_INFO (wincrypt.h)
description: Represents key-encryption key information when using Elliptic Curve Cryptography (ECC) in the Cryptographic Message Syntax (CMS) EnvelopedData content type.
helpviewer_keywords: ["*PCRYPT_ECC_CMS_SHARED_INFO","CRYPT_ECC_CMS_SHARED_INFO","CRYPT_ECC_CMS_SHARED_INFO structure [Security]","CRYPT_ECC_CMS_SHARED_INFO_SUPPPUBINFO_BYTE_LENGTH","PCRYPT_ECC_CMS_SHARED_INFO","PCRYPT_ECC_CMS_SHARED_INFO structure pointer [Security]","security.crypt_ecc_cms_shared_info","wincrypt/CRYPT_ECC_CMS_SHARED_INFO","wincrypt/PCRYPT_ECC_CMS_SHARED_INFO"]
old-location: security\crypt_ecc_cms_shared_info.htm
tech.root: security
ms.assetid: 858dbf61-5c4f-4bd6-b47c-0a1379119693
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_ECC_CMS_SHARED_INFO, CRYPT_ECC_CMS_SHARED_INFO, CRYPT_ECC_CMS_SHARED_INFO structure [Security], CRYPT_ECC_CMS_SHARED_INFO_SUPPPUBINFO_BYTE_LENGTH, PCRYPT_ECC_CMS_SHARED_INFO, PCRYPT_ECC_CMS_SHARED_INFO structure pointer [Security], security.crypt_ecc_cms_shared_info, wincrypt/CRYPT_ECC_CMS_SHARED_INFO, wincrypt/PCRYPT_ECC_CMS_SHARED_INFO'
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
req.typenames: CRYPT_ECC_CMS_SHARED_INFO, *PCRYPT_ECC_CMS_SHARED_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_ECC_CMS_SHARED_INFO
 - wincrypt/_CRYPT_ECC_CMS_SHARED_INFO
 - PCRYPT_ECC_CMS_SHARED_INFO
 - wincrypt/PCRYPT_ECC_CMS_SHARED_INFO
 - CRYPT_ECC_CMS_SHARED_INFO
 - wincrypt/CRYPT_ECC_CMS_SHARED_INFO
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
 - CRYPT_ECC_CMS_SHARED_INFO
---

# CRYPT_ECC_CMS_SHARED_INFO structure


## -description

The <b>CRYPT_ECC_CMS_SHARED_INFO</b> structure represents key-encryption key information when using Elliptic Curve Cryptography (ECC) in the Cryptographic Message Syntax (CMS) EnvelopedData content type. This structure is used in a key-exchange scenario for exchange of keys to encrypt and decrypt content.  A pointer to this structure can be used in the <i>pvStructInfo</i> parameter of <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> or <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> and is specified by the constant <b>ECC_CMS_SHARED_INFO</b>. For more information, see <a href="/windows/desktop/SecCrypto/constants-for-cryptencodeobject-and-cryptdecodeobject">Constants for CryptEncodeObject and CryptDecodeObject</a>.

## -struct-fields

### -field Algorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the object identifier of the key-encryption algorithm used to wrap the content-encryption key.

### -field EntityUInfo

An optional member that contains additional user keying material as an octet string supplied by the sending agent.

### -field rgbSuppPubInfo

An array of four bytes that represent the length, in bits, of the key-encryption key. The byte array is in <a href="/windows/desktop/SecGloss/l-gly">little-endian</a> order.


The following table contains the definition of the array dimension.





#### CRYPT_ECC_CMS_SHARED_INFO_SUPPPUBINFO_BYTE_LENGTH (4)

## -see-also

<a href="https://www.ietf.org/rfc/rfc3278.txt">RFC 3278</a>