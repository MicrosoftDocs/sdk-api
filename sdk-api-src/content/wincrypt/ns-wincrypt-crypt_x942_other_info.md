---
UID: NS:wincrypt._CRYPT_X942_OTHER_INFO
title: CRYPT_X942_OTHER_INFO (wincrypt.h)
author: windows-sdk-content
description: The CRYPT_X942_OTHER_INFO structure contains additional key generation information.
old-location: security\crypt_x942_other_info.htm
tech.root: SecCrypto
ms.assetid: 7761af36-ad16-4628-86cb-16cbded6fb69
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCRYPT_X942_OTHER_INFO, CRYPT_X942_OTHER_INFO, CRYPT_X942_OTHER_INFO structure [Security], PCRYPT_X942_OTHER_INFO, PCRYPT_X942_OTHER_INFO structure pointer [Security], _crypto2_crypt_x942_other_info, security.crypt_x942_other_info, wincrypt/CRYPT_X942_OTHER_INFO, wincrypt/PCRYPT_X942_OTHER_INFO"
ms.topic: struct
f1_keywords: 
 - "wincrypt/CRYPT_X942_OTHER_INFO"
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
targetos: Windows
req.typenames: CRYPT_X942_OTHER_INFO, *PCRYPT_X942_OTHER_INFO
req.redist: 
ms.custom: 19H1
---

# CRYPT_X942_OTHER_INFO structure


## -description


The <b>CRYPT_X942_OTHER_INFO</b> structure contains additional key generation information.


## -struct-fields




### -field pszContentEncryptionObjId

OID of the content encryption algorithm.


### -field rgbCounter

Array of BYTES of length <b>CRYPT_X942_COUNTER_BYTE_LENGTH</b>. The value is stored in <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">little-endian</a> order.


### -field rgbKeyLength

Array of BYTES of length <b>CRYPT_X942_KEY_LENGTH_BYTE_LENGTH</b>. The value is stored in little-endian order.


### -field PubInfo

Optional <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> for additional information.

