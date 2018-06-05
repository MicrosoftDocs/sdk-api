---
UID: NS:wincrypt._CRYPT_ATTRIBUTES
title: "_CRYPT_ATTRIBUTES"
author: windows-sdk-content
description: Contains an array of attributes.
old-location: security\crypt_attributes.htm
old-project: SecCrypto
ms.assetid: 782f3022-d852-4ad7-8e0f-afbccc25928a
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCMSG_ATTR, *PCRYPT_ATTRIBUTES, CMSG_ATTR, CMSG_ATTR structure [Security], CRYPT_ATTRIBUTES, CRYPT_ATTRIBUTES structure [Security], PCRYPT_ATTRIBUTES, PCRYPT_ATTRIBUTES structure pointer [Security], _CRYPT_ATTRIBUTES, _crypto2_crypt_attributes, security.crypt_attributes, wincrypt/CMSG_ATTR, wincrypt/CRYPT_ATTRIBUTES, wincrypt/PCRYPT_ATTRIBUTES"
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
tech.root: 
req.typenames: CRYPT_ATTRIBUTES, *PCRYPT_ATTRIBUTES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CRYPT_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_ATTRIBUTES structure


## -description


<p class="CCE_Message">[The <b>CRYPT_ATTRIBUTES</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_ATTRIBUTES</b> structure contains an array of attributes.


## -struct-fields




### -field cAttr

Number of elements in the <b>rgAttr</b> array.


### -field rgAttr

Array of 
<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/eae631d2-5e5f-4964-b079-9692831b34fc">CMSG_SIGNER_INFO</a>



<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/5a05eb09-208f-4e94-abfa-c2f14c0a3164">CryptMsgGetParam</a>
 

 

