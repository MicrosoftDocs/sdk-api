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

# _CMSG_RC2_AUX_INFO structure


## -description


The <b>CMSG_RC2_AUX_INFO</b> structure contains the bit length of the key for RC2 encryption algorithms. The <b>pvEncryptionAuxInfo</b> member in <a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a> can be set to point to an instance of this structure.
<div class="alert"><b>Note</b>  This structure is only used when the other members of a <a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a> structure indicate that a default key length of 40 bits is to be used with an RC2 encryption algorithm. For more information, see 
<b>CMSG_ENVELOPED_ENCODE_INFO</b>.</div><div> </div>

## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field dwBitLen

Specifies the RC2 effective key length. Currently 40-, 64-, and 128-bit lengths are supported. 




<div class="alert"><b>Note</b>  This value is the actual key bit length to be used. The values of the <b>dwVersion</b> member of a 
<a href="https://msdn.microsoft.com/58b1dc44-55ea-4c22-a115-dfeaee8a2297">CRYPT_RC2_CBC_PARAMETERS</a> structure to indicate the use of a specific key length is not that specific key length. For example, the <b>dwVersion</b> value that indicates the use of a 128-bit key length is CRYPT_RC2_128BIT_VERSION, which is defined as 58, not 128 bits.</div>
<div> </div>
<div class="alert"><b>Note</b>  If <b>dwBitLen</b> is set to CMSG_SP3_COMPATIBLE_ENCRYPT_FLAG, SP3 compatible encryption is done and the 40-bit default length is ignored.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>
 

 

