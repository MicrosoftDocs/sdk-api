---
UID: NS:bcrypt._BCRYPT_DH_PARAMETER_HEADER
title: "_BCRYPT_DH_PARAMETER_HEADER"
author: windows-sdk-content
description: Used to contain parameter header information for a Diffie-Hellman key.
old-location: security\bcrypt_dh_parameter_header.htm
old-project: seccng
ms.assetid: 5d023653-6197-4f08-8c71-e1d10f6b1860
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BCRYPT_DH_PARAMETERS_MAGIC, BCRYPT_DH_PARAMETER_HEADER, BCRYPT_DH_PARAMETER_HEADER structure [Security], _BCRYPT_DH_PARAMETER_HEADER, bcrypt/BCRYPT_DH_PARAMETER_HEADER, security.bcrypt_dh_parameter_header
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BCRYPT_DH_PARAMETER_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_DH_PARAMETER_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

