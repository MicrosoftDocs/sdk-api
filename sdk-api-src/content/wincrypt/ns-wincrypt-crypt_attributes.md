---
UID: NS:wincrypt._CRYPT_ATTRIBUTES
title: CRYPT_ATTRIBUTES (wincrypt.h)
author: windows-sdk-content
description: Contains an array of attributes.
old-location: security\crypt_attributes.htm
tech.root: SecCrypto
ms.assetid: 782f3022-d852-4ad7-8e0f-afbccc25928a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PCMSG_ATTR, *PCRYPT_ATTRIBUTES, CMSG_ATTR, CMSG_ATTR structure [Security], CRYPT_ATTRIBUTES, CRYPT_ATTRIBUTES structure [Security], PCRYPT_ATTRIBUTES, PCRYPT_ATTRIBUTES structure pointer [Security], _crypto2_crypt_attributes, security.crypt_attributes, wincrypt/CMSG_ATTR, wincrypt/CRYPT_ATTRIBUTES, wincrypt/PCRYPT_ATTRIBUTES'
ms.topic: struct
f1_keywords:
- wincrypt/CRYPT_ATTRIBUTES
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
- CRYPT_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: CRYPT_ATTRIBUTES, *PCRYPT_ATTRIBUTES
req.redist: 
ms.custom: 19H1
---

# CRYPT_ATTRIBUTES structure


## -description


<p class="CCE_Message">[The <b>CRYPT_ATTRIBUTES</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_ATTRIBUTES</b> structure contains an array of attributes.


## -struct-fields




### -field cAttr

Number of elements in the <b>rgAttr</b> array.


### -field rgAttr

Array of 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_info">CMSG_SIGNER_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsggetparam">CryptMsgGetParam</a>
 

 

