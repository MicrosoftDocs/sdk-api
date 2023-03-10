---
UID: NS:bcrypt._BCRYPT_DSA_PARAMETER_HEADER
title: BCRYPT_DSA_PARAMETER_HEADER (bcrypt.h)
description: Used to contain parameter header information for a Digital Signature Algorithm (DSA) key.
helpviewer_keywords: ["BCRYPT_DSA_PARAMETERS_MAGIC","BCRYPT_DSA_PARAMETER_HEADER","BCRYPT_DSA_PARAMETER_HEADER structure [Security]","PBCRYPT_DSA_PARAMETER_HEADER","PBCRYPT_DSA_PARAMETER_HEADER structure pointer [Security]","bcrypt/BCRYPT_DSA_PARAMETER_HEADER","bcrypt/PBCRYPT_DSA_PARAMETER_HEADER","security.bcrypt_dsa_parameter_header"]
old-location: security\bcrypt_dsa_parameter_header.htm
tech.root: security
ms.assetid: 96c20afb-e429-45b3-b817-88134914a26b
ms.date: 12/05/2018
ms.keywords: BCRYPT_DSA_PARAMETERS_MAGIC, BCRYPT_DSA_PARAMETER_HEADER, BCRYPT_DSA_PARAMETER_HEADER structure [Security], PBCRYPT_DSA_PARAMETER_HEADER, PBCRYPT_DSA_PARAMETER_HEADER structure pointer [Security], bcrypt/BCRYPT_DSA_PARAMETER_HEADER, bcrypt/PBCRYPT_DSA_PARAMETER_HEADER, security.bcrypt_dsa_parameter_header
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
req.typenames: BCRYPT_DSA_PARAMETER_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_DSA_PARAMETER_HEADER
 - bcrypt/_BCRYPT_DSA_PARAMETER_HEADER
 - BCRYPT_DSA_PARAMETER_HEADER
 - bcrypt/BCRYPT_DSA_PARAMETER_HEADER
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
 - BCRYPT_DSA_PARAMETER_HEADER
---

# BCRYPT_DSA_PARAMETER_HEADER structure


## -description

The <b>BCRYPT_DSA_PARAMETER_HEADER</b> structure is used as a header for a <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Algorithm</a> (DSA) parameters <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> containing information for generating a DSA key. This structure is used with the <a href="/windows/desktop/SecCNG/cng-property-identifiers">BCRYPT_DSA_PARAMETERS</a> property in the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a> function.

## -struct-fields

### -field cbLength

The total size, in bytes, of this structure and the buffer that immediately follows this structure in memory.

### -field dwMagic

The magic value for the key.


This member must be the following value.





#### BCRYPT_DSA_PARAMETERS_MAGIC (0x4d505344)

### -field cbKeyLength

The size, in bytes, of the key that this structure applies to.

### -field Count

The number of iterations performed to generate the prime number <i>q</i> from the seed.

### -field Seed

The seed value, in big-endian format, used to generate <i>q</i>.

### -field q

The 160-bit prime factor, in big-endian format.

## -remarks

When using this structure in a <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a> call, to set the parameters for a DSA key created in a <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgeneratekeypair">BCryptGenerateKeyPair</a> call, (cbKeyLength*8) must equal the previously set dwLength.

The structure applies to DSA keys that equal or exceed 512 bits in length but are less than or equal to 1024 bits.

This structure is used as a header for a larger buffer. The DSA parameters blob has the following format in contiguous memory. The Modulus and Generator are in big-endian format.


``` syntax

BCRYPT_DSA_PARAMETER_HEADER
Modulus[cbKeyLength]    // Big-endian.
Generator[cbKeyLength]  // Big-endian.

```


## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgeneratekeypair">BCryptGenerateKeyPair</a>

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a>

<a href="/windows/desktop/SecCNG/cng-property-identifiers">Cryptography Primitive Property Identifiers</a>
