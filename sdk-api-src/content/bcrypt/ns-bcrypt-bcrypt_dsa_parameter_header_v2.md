---
UID: NS:bcrypt._BCRYPT_DSA_PARAMETER_HEADER_V2
title: BCRYPT_DSA_PARAMETER_HEADER_V2 (bcrypt.h)
description: Contains parameter header information for a Digital Signature Algorithm (DSA) key.
helpviewer_keywords: ["BCRYPT_DSA_PARAMETERS_MAGIC_V2","BCRYPT_DSA_PARAMETER_HEADER_V2","BCRYPT_DSA_PARAMETER_HEADER_V2 structure [Security]","PBCRYPT_DSA_PARAMETER_HEADER_V2","PBCRYPT_DSA_PARAMETER_HEADER_V2 structure pointer [Security]","bcrypt/BCRYPT_DSA_PARAMETER_HEADER_V2","bcrypt/PBCRYPT_DSA_PARAMETER_HEADER_V2","security.bcrypt_dsa_parameter_header_v2"]
old-location: security\bcrypt_dsa_parameter_header_v2.htm
tech.root: security
ms.assetid: 25FF89D8-1E3E-433B-AC5C-1CADC09A49D0
ms.date: 12/05/2018
ms.keywords: BCRYPT_DSA_PARAMETERS_MAGIC_V2, BCRYPT_DSA_PARAMETER_HEADER_V2, BCRYPT_DSA_PARAMETER_HEADER_V2 structure [Security], PBCRYPT_DSA_PARAMETER_HEADER_V2, PBCRYPT_DSA_PARAMETER_HEADER_V2 structure pointer [Security], bcrypt/BCRYPT_DSA_PARAMETER_HEADER_V2, bcrypt/PBCRYPT_DSA_PARAMETER_HEADER_V2, security.bcrypt_dsa_parameter_header_v2
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: BCRYPT_DSA_PARAMETER_HEADER_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_DSA_PARAMETER_HEADER_V2
 - bcrypt/_BCRYPT_DSA_PARAMETER_HEADER_V2
 - BCRYPT_DSA_PARAMETER_HEADER_V2
 - bcrypt/BCRYPT_DSA_PARAMETER_HEADER_V2
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
 - BCRYPT_DSA_PARAMETER_HEADER_V2
---

# BCRYPT_DSA_PARAMETER_HEADER_V2 structure


## -description

The <b>BCRYPT_DSA_PARAMETER_HEADER_V2</b> structure is used as a header for a <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Algorithm</a> (DSA) parameters <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> containing information for generating a DSA key. This structure is used with the <a href="/windows/desktop/SecCNG/cng-property-identifiers">BCRYPT_DSA_PARAMETERS</a> property in the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a> function.

## -struct-fields

### -field cbLength

The total size, in bytes, of this structure and the buffer that immediately follows this structure in memory.

### -field dwMagic

The magic value for the key.


This member must be the following value.





#### BCRYPT_DSA_PARAMETERS_MAGIC_V2 (0x324d5044)

### -field cbKeyLength

The size, in bytes, of the key that this structure applies to.

### -field hashAlgorithm

A <a href="/windows/desktop/api/bcrypt/ne-bcrypt-hashalgorithm_enum">HASHALGORITHM_ENUM</a> enumeration value that specifies the hashing algorithm to use.

### -field standardVersion

A <a href="/windows/desktop/api/bcrypt/ne-bcrypt-dsafipsversion_enum">DSAFIPSVERSION_ENUM</a> enumeration value that specifies the Federal Information Processing Standard (FIPS) to apply.

### -field cbSeedLength

Length of the seed used to generate the prime number <i>q</i> in bytes.

### -field cbGroupSize

Size of the prime number <i>q</i>. Currently, when the key exceeds 1024 bits in length, <i>q</i> is 32 bytes long.

### -field Count

The number of iterations performed to generate the prime number q from the seed. For more information, see NIST standard FIPS186-3.

## -remarks

When using this structure in a <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a> call, to set the parameters for a DSA key created in a <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgeneratekeypair">BCryptGenerateKeyPair</a> call, (cbKeyLength*8) must equal the previously set dwLength.

The structure applies to DSA keys that exceed 1024 bits in length but are less than or equal to 3072 bits.

This structure is used as a header for a larger buffer. The DSA parameters blob has the following format in contiguous memory. The Seed, q, Modulus, and Generator are in big-endian format.


``` syntax

BCRYPT_DSA_PARAMETER_HEADER_V2
Seed[cbSeedLength]      // Big-endian.
q[cbGroupSize]          // Big-endian.
Modulus[cbKeyLength]    // Big-endian.
Generator[cbKeyLength]  // Big-endian.

```


## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgeneratekeypair">BCryptGenerateKeyPair</a>

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a>

<a href="/windows/desktop/SecCNG/cng-property-identifiers">Cryptography Primitive Property Identifiers</a>
