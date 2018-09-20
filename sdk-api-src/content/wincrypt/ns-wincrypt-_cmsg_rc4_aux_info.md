---
UID: NS:wincrypt._CMSG_RC4_AUX_INFO
title: "_CMSG_RC4_AUX_INFO"
author: windows-sdk-content
description: The CMSG_RC4_AUX_INFO structure contains the bit length of the key for RC4 encryption algorithms. The pvEncryptionAuxInfo member in CMSG_ENVELOPED_ENCODE_INFO can be set to point to an instance of this structure.
old-location: security\cmsg_rc4_aux_info.htm
tech.root: seccrypto
ms.assetid: 8e456156-b84a-4ca7-9dc7-9f5da4a32a6c
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: "*PCMSG_RC4_AUX_INFO, CMSG_RC4_AUX_INFO, CMSG_RC4_AUX_INFO structure [Security], PCMSG_RC4_AUX_INFO, PCMSG_RC4_AUX_INFO structure pointer [Security], _CMSG_RC4_AUX_INFO, _crypto2_cmsg_rc4_aux_info, security.cmsg_rc4_aux_info, wincrypt/CMSG_RC4_AUX_INFO, wincrypt/PCMSG_RC4_AUX_INFO"
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
 - CMSG_RC4_AUX_INFO
product: Windows
targetos: Windows
req.typenames: CMSG_RC4_AUX_INFO, *PCMSG_RC4_AUX_INFO
req.redist: 
---

# _CMSG_RC4_AUX_INFO structure


## -description


The <b>CMSG_RC4_AUX_INFO</b> structure contains the bit length of the key for RC4 encryption algorithms. The <b>pvEncryptionAuxInfo</b> member in <a href="https://msdn.microsoft.com/87712541-2806-4709-a7cf-c9ba966c96fd">CMSG_ENVELOPED_ENCODE_INFO</a> can be set to point to an instance of this structure.


## -struct-fields




### -field cbSize

Size of this structure in bytes.


### -field dwBitLen

Determines the RC4 <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">salt length</a>. If set to CMSG_RC4_NO_SALT_FLAG, no salt is generated. For any other value, (128 - the length set) /8 bytes of salt are generated and encoded as an OCTET STRING in the algorithm parameters field.

