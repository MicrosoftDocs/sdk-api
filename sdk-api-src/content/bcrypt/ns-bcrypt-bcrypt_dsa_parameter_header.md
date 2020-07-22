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
f1_keywords:
- bcrypt/BCRYPT_DSA_PARAMETER_HEADER
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Bcrypt.h
api_name:
- BCRYPT_DSA_PARAMETER_HEADER
targetos: Windows
req.typenames: BCRYPT_DSA_PARAMETER_HEADER
req.redist: 
ms.custom: 19H1
---

# BCRYPT_DSA_PARAMETER_HEADER structure


## -description


The <b>BCRYPT_DSA_PARAMETER_HEADER</b> structure is used to contain parameter header information for a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Digital Signature Algorithm</a> (DSA) key. This structure is used with the <a href="https://docs.microsoft.com/windows/desktop/SecCNG/cng-property-identifiers">BCRYPT_DSA_PARAMETERS</a> property in the <a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a> function.


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



This structure is used as a header for a larger buffer. 

The single memory block consists of the following items:

<ul>
<li>This structure followed by a buffer of <b>cbKeyLength</b> size that contains the DSA prime number, in big-endian format.</li>
<li>Another buffer of <b>cbKeyLength</b> size that contains the DSA generator number, in big-endian format.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsetproperty">BCryptSetProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCNG/cng-property-identifiers">Cryptography Primitive Property Identifiers</a>
 

 

