---
UID: NS:wincrypt._CMSG_RC2_AUX_INFO
title: "_CMSG_RC2_AUX_INFO"
author: windows-sdk-content
description: Contains the bit length of the key for RC2 encryption algorithms.
old-location: security\cmsg_rc2_aux_info.htm
tech.root: seccrypto
ms.assetid: 6d7014fa-2d0c-48de-bda5-91d19ad879f9
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: "*PCMSG_RC2_AUX_INFO, CMSG_RC2_AUX_INFO, CMSG_RC2_AUX_INFO structure [Security], PCMSG_RC2_AUX_INFO, PCMSG_RC2_AUX_INFO structure pointer [Security], _CMSG_RC2_AUX_INFO, _crypto2_cmsg_rc2_aux_info, security.cmsg_rc2_aux_info, wincrypt/CMSG_RC2_AUX_INFO, wincrypt/PCMSG_RC2_AUX_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Wincrypt.h
api_name:
 - CMSG_RC2_AUX_INFO
product: Windows
targetos: Windows
req.typenames: CMSG_RC2_AUX_INFO, *PCMSG_RC2_AUX_INFO
req.redist: 
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
 

 

