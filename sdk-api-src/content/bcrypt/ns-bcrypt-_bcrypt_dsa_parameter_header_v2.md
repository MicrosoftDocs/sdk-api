---
UID: NS:bcrypt._BCRYPT_DSA_PARAMETER_HEADER_V2
title: "_BCRYPT_DSA_PARAMETER_HEADER_V2"
author: windows-driver-content
description: Contains parameter header information for a Digital Signature Algorithm (DSA) key.
old-location: security\bcrypt_dsa_parameter_header_v2.htm
old-project: SecCNG
ms.assetid: 25FF89D8-1E3E-433B-AC5C-1CADC09A49D0
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: BCRYPT_DSA_PARAMETERS_MAGIC_V2, BCRYPT_DSA_PARAMETER_HEADER_V2, BCRYPT_DSA_PARAMETER_HEADER_V2 structure [Security], PBCRYPT_DSA_PARAMETER_HEADER_V2, PBCRYPT_DSA_PARAMETER_HEADER_V2 structure pointer [Security], _BCRYPT_DSA_PARAMETER_HEADER_V2, bcrypt/BCRYPT_DSA_PARAMETER_HEADER_V2, bcrypt/PBCRYPT_DSA_PARAMETER_HEADER_V2, security.bcrypt_dsa_parameter_header_v2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: BCRYPT_DSA_PARAMETER_HEADER_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bcrypt.h
api_name:
-	BCRYPT_DSA_PARAMETER_HEADER_V2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BCRYPT_DSA_PARAMETER_HEADER_V2 structure


## -description


The <b>BCRYPT_DSA_PARAMETER_HEADER_V2</b> structure is contains parameter header information for a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA) key. This structure is used with the <a href="https://msdn.microsoft.com/ebcc8202-94b4-47ad-9918-e5bc843a258f">BCRYPT_DSA_PARAMETERS</a> property in the <a href="https://msdn.microsoft.com/687f3410-d28b-4ce2-a2a1-c564f757c668">BCryptSetProperty</a> function.


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

A <a href="https://msdn.microsoft.com/482DA4B6-EC1C-4E88-95C0-62ED1356DC3B">HASHALGORITHM_ENUM</a> enumeration value that specifies the hashing algorithm to use.


### -field standardVersion

A <a href="https://msdn.microsoft.com/6797D7C0-3451-464E-9261-61217ADAB9C1">DSAFIPSVERSION_ENUM</a> enumeration value that specifies the Federal Information Processing Standard(FIPS) to apply.


### -field cbSeedLength

Length of the seed used to generate the prime number q.


### -field cbGroupSize

Size of the prime number q . Currently, if the key is less than 128 bits, q is 20 bytes long. If the key exceeds 256 bits, q is 32 bytes long.


### -field Count

The number of iterations performed to generate the prime number q from the seed. For more information, see NIST standard FIPS186-3.


## -see-also




<a href="https://msdn.microsoft.com/687f3410-d28b-4ce2-a2a1-c564f757c668">BCryptSetProperty</a>



<a href="https://msdn.microsoft.com/ebcc8202-94b4-47ad-9918-e5bc843a258f">Cryptography Primitive Property Identifiers</a>
 

 

