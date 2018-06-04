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

# _BCRYPT_DH_PARAMETER_HEADER structure


## -description


The <b>BCRYPT_DH_PARAMETER_HEADER</b> structure is used to contain parameter header information for a Diffie-Hellman key. This structure is used with the <a href="https://msdn.microsoft.com/ebcc8202-94b4-47ad-9918-e5bc843a258f">BCRYPT_DH_PARAMETERS</a> property in the <a href="https://msdn.microsoft.com/687f3410-d28b-4ce2-a2a1-c564f757c668">BCryptSetProperty</a> function.


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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// In this example, the rgbModulus variable is a byte array that contains the modulus in big-endian byte order. 
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
pDHParamHeader-&gt;cbLength = cbDHParams;
pDHParamHeader-&gt;cbKeyLength = cbKeySize;
pDHParamHeader-&gt;dwMagic = BCRYPT_DH_PARAMETERS_MAGIC;

// Add the modulus to the parameters.
// The rgbModulus argument is a byte array that contains the modulus.
PBYTE pbTemp = (PBYTE)pbDHParams + sizeof(BCRYPT_DH_PARAMETER_HEADER);
CopyMemory(pbTemp, rgbModulus, pDHParamHeader-&gt;cbKeyLength);

// Add the generator to the parameters.
// The rgbGenerator argument is a byte array that contains the generator.
pbTemp += pDHParamHeader-&gt;cbKeyLength;
CopyMemory(pbTemp, rgbGenerator, pDHParamHeader-&gt;cbKeyLength);

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/687f3410-d28b-4ce2-a2a1-c564f757c668">BCryptSetProperty</a>



<a href="https://msdn.microsoft.com/ebcc8202-94b4-47ad-9918-e5bc843a258f">Cryptography Primitive Property Identifiers</a>
 

 

