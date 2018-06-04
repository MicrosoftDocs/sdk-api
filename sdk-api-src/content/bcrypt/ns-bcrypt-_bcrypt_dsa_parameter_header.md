---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

