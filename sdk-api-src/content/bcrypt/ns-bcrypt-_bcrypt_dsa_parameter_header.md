---
UID: NS:bcrypt._BCRYPT_DSA_PARAMETER_HEADER
title: "_BCRYPT_DSA_PARAMETER_HEADER"
author: windows-driver-content
description: Used to contain parameter header information for a Digital Signature Algorithm (DSA) key.
old-location: security\bcrypt_dsa_parameter_header.htm
old-project: SecCNG
ms.assetid: 96c20afb-e429-45b3-b817-88134914a26b
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: BCRYPT_DSA_PARAMETERS_MAGIC, BCRYPT_DSA_PARAMETER_HEADER, BCRYPT_DSA_PARAMETER_HEADER structure [Security], PBCRYPT_DSA_PARAMETER_HEADER, PBCRYPT_DSA_PARAMETER_HEADER structure pointer [Security], _BCRYPT_DSA_PARAMETER_HEADER, bcrypt/BCRYPT_DSA_PARAMETER_HEADER, bcrypt/PBCRYPT_DSA_PARAMETER_HEADER, security.bcrypt_dsa_parameter_header
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: BCRYPT_DSA_PARAMETER_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bcrypt.h
api_name:
-	BCRYPT_DSA_PARAMETER_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BCRYPT_DSA_PARAMETER_HEADER structure


## -description


The <b>BCRYPT_DSA_PARAMETER_HEADER</b> structure is used to contain parameter header information for a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Digital Signature Algorithm</a> (DSA) key. This structure is used with the <a href="https://msdn.microsoft.com/ebcc8202-94b4-47ad-9918-e5bc843a258f">BCRYPT_DSA_PARAMETERS</a> property in the <a href="https://msdn.microsoft.com/687f3410-d28b-4ce2-a2a1-c564f757c668">BCryptSetProperty</a> function.


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




<a href="https://msdn.microsoft.com/687f3410-d28b-4ce2-a2a1-c564f757c668">BCryptSetProperty</a>



<a href="https://msdn.microsoft.com/ebcc8202-94b4-47ad-9918-e5bc843a258f">Cryptography Primitive Property Identifiers</a>
 

 

