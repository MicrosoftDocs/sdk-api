---
UID: NE:bcrypt.HASHALGORITHM_ENUM
title: HASHALGORITHM_ENUM (bcrypt.h)
description: Specifies signing and hashing algorithms.
helpviewer_keywords: ["DSA_HASH_ALGORITHM_SHA1","DSA_HASH_ALGORITHM_SHA256","DSA_HASH_ALGORITHM_SHA512","HASHALGORITHM_ENUM","HASHALGORITHM_ENUM enumeration [Security]","bcrypt/DSA_HASH_ALGORITHM_SHA1","bcrypt/DSA_HASH_ALGORITHM_SHA256","bcrypt/DSA_HASH_ALGORITHM_SHA512","bcrypt/HASHALGORITHM_ENUM","security.hashalgorithm_enum"]
old-location: security\hashalgorithm_enum.htm
tech.root: security
ms.assetid: 482DA4B6-EC1C-4E88-95C0-62ED1356DC3B
ms.date: 12/05/2018
ms.keywords: DSA_HASH_ALGORITHM_SHA1, DSA_HASH_ALGORITHM_SHA256, DSA_HASH_ALGORITHM_SHA512, HASHALGORITHM_ENUM, HASHALGORITHM_ENUM enumeration [Security], bcrypt/DSA_HASH_ALGORITHM_SHA1, bcrypt/DSA_HASH_ALGORITHM_SHA256, bcrypt/DSA_HASH_ALGORITHM_SHA512, bcrypt/HASHALGORITHM_ENUM, security.hashalgorithm_enum
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HASHALGORITHM_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HASHALGORITHM_ENUM
 - bcrypt/HASHALGORITHM_ENUM
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
 - HASHALGORITHM_ENUM
---

# HASHALGORITHM_ENUM enumeration


## -description

The <b>HASHALGORITHM_ENUM</b> enumeration type specifies signing and hashing algorithms. It is used by the <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob_v2">BCRYPT_DSA_KEY_BLOB_V2</a> and <a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2">BCRYPT_DSA_PARAMETER_HEADER_V2</a> structures.

## -enum-fields

### -field DSA_HASH_ALGORITHM_SHA1

Represents a Digital Signature Algorithm (DSA) that uses the Secure Hashing Algorithm 1 (SHA1) to hash the message contents before signing.

### -field DSA_HASH_ALGORITHM_SHA256

Represents a Digital Signature Algorithm (DSA) that uses the Secure Hashing Algorithm 256 (SHA256) to hash the message contents before signing.

### -field DSA_HASH_ALGORITHM_SHA512

Represents a Digital Signature Algorithm (DSA) that uses the Secure Hashing Algorithm 512 (SHA512) to hash the message contents before signing.

## -see-also

<a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_key_blob_v2">BCRYPT_DSA_KEY_BLOB_V2</a>



<a href="/windows/desktop/api/bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2">BCRYPT_DSA_PARAMETER_HEADER_V2</a>

