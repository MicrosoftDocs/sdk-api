---
UID: NS:wincrypt._CRYPT_X942_OTHER_INFO
title: "_CRYPT_X942_OTHER_INFO"
author: windows-sdk-content
description: The CRYPT_X942_OTHER_INFO structure contains additional key generation information.
old-location: security\crypt_x942_other_info.htm
tech.root: seccrypto
ms.assetid: 7761af36-ad16-4628-86cb-16cbded6fb69
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PCRYPT_X942_OTHER_INFO, CRYPT_X942_OTHER_INFO, CRYPT_X942_OTHER_INFO structure [Security], PCRYPT_X942_OTHER_INFO, PCRYPT_X942_OTHER_INFO structure pointer [Security], _CRYPT_X942_OTHER_INFO, _crypto2_crypt_x942_other_info, security.crypt_x942_other_info, wincrypt/CRYPT_X942_OTHER_INFO, wincrypt/PCRYPT_X942_OTHER_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CRYPT_X942_OTHER_INFO
product: Windows
targetos: Windows
req.typenames: CRYPT_X942_OTHER_INFO, *PCRYPT_X942_OTHER_INFO
req.redist: 
---

# _CRYPT_X942_OTHER_INFO structure


## -description


The <b>CRYPT_X942_OTHER_INFO</b> structure contains additional key generation information.


## -struct-fields




### -field pszContentEncryptionObjId

OID of the content encryption algorithm.


### -field rgbCounter

Array of BYTES of length <b>CRYPT_X942_COUNTER_BYTE_LENGTH</b>. The value is stored in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a> order.


### -field rgbKeyLength

Array of BYTES of length <b>CRYPT_X942_KEY_LENGTH_BYTE_LENGTH</b>. The value is stored in little-endian order.


### -field PubInfo

Optional <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> for additional information.

