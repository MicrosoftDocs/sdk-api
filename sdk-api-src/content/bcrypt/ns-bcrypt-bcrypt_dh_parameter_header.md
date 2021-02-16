---
UID: NS:bcrypt._BCRYPT_DH_PARAMETER_HEADER
title: BCRYPT_DH_PARAMETER_HEADER (bcrypt.h)
description: Used to contain parameter header information for a Diffie-Hellman key.
helpviewer_keywords: ["BCRYPT_DH_PARAMETERS_MAGIC","BCRYPT_DH_PARAMETER_HEADER","BCRYPT_DH_PARAMETER_HEADER structure [Security]","bcrypt/BCRYPT_DH_PARAMETER_HEADER","security.bcrypt_dh_parameter_header"]
old-location: security\bcrypt_dh_parameter_header.htm
tech.root: security
ms.assetid: 5d023653-6197-4f08-8c71-e1d10f6b1860
ms.date: 12/05/2018
ms.keywords: BCRYPT_DH_PARAMETERS_MAGIC, BCRYPT_DH_PARAMETER_HEADER, BCRYPT_DH_PARAMETER_HEADER structure [Security], bcrypt/BCRYPT_DH_PARAMETER_HEADER, security.bcrypt_dh_parameter_header
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
req.typenames: BCRYPT_DH_PARAMETER_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_DH_PARAMETER_HEADER
 - bcrypt/_BCRYPT_DH_PARAMETER_HEADER
 - BCRYPT_DH_PARAMETER_HEADER
 - bcrypt/BCRYPT_DH_PARAMETER_HEADER
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
 - BCRYPT_DH_PARAMETER_HEADER
---

# BCRYPT_DH_PARAMETER_HEADER structure


## -description

The <b>BCRYPT_DH_PARAMETER_HEADER</b> structure is used to contain parameter header information for a Diffie-Hellman key. This structure is used with the <a href="/windows/desktop/SecCNG/cng-property-identifiers">BCRYPT_DH_PARAMETERS</a> property in the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a> function.

## -struct-fields

### -field cbLength

The total size, in bytes, of this structure and the buffer that immediately follows this structure in memory.

### -field dwMagic

The magic value for the key.


This member must be the following value.





#### BCRYPT_DH_PARAMETERS_MAGIC (0x4d504844)

### -field cbKeyLength

The size, in bytes, of the key that this structure applies to.

## -remarks

This structure is used as a header for a larger buffer. The single memory block consists of this structure followed by a buffer of <b>cbKeyLength</b> size that contains the Diffie-Hellman prime number, and another buffer of <b>cbKeyLength</b> size that contains the Diffie-Hellman generator number. Both of these numbers are in big-endian format.

The following example shows how to calculate the sizes needed for this buffer and how to fill in the members of this structure.


```cpp
// In this example, the rgbModulus variable is a byte array that contains the modulus in big-endian byte order. 
// The rgbGenerator variable is a byte array that contains the generator in big-endian byte order.

ULONG cbDHParams = sizeof(BCRYPT_DH_PARAMETER_HEADER) +     (cbKeySize * 2);
PBYTE pbDHParams = (PBYTE)malloc(cbDHParams);
if(!pbDHParams)
{
    status = STATUS_NO_MEMORY;
    goto Cleanup;
}

BCRYPT_DH_PARAMETER_HEADER *pDHParamHeader;
pDHParamHeader = (BCRYPT_DH_PARAMETER_HEADER*)pbDHParams;
pDHParamHeader->cbLength = cbDHParams;
pDHParamHeader->cbKeyLength = cbKeySize;
pDHParamHeader->dwMagic = BCRYPT_DH_PARAMETERS_MAGIC;

// Add the modulus to the parameters.
// The rgbModulus argument is a byte array that contains the modulus.
PBYTE pbTemp = (PBYTE)pbDHParams + sizeof(BCRYPT_DH_PARAMETER_HEADER);
CopyMemory(pbTemp, rgbModulus, pDHParamHeader->cbKeyLength);

// Add the generator to the parameters.
// The rgbGenerator argument is a byte array that contains the generator.
pbTemp += pDHParamHeader->cbKeyLength;
CopyMemory(pbTemp, rgbGenerator, pDHParamHeader->cbKeyLength);


```

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a>



<a href="/windows/desktop/SecCNG/cng-property-identifiers">Cryptography Primitive Property Identifiers</a>