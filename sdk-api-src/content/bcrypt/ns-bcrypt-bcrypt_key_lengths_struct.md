---
UID: NS:bcrypt.__BCRYPT_KEY_LENGTHS_STRUCT
title: BCRYPT_KEY_LENGTHS_STRUCT (bcrypt.h)
author: windows-sdk-content
description: Defines the range of key sizes that are supported by the provider.
old-location: security\bcrypt_key_lengths_struct.htm
tech.root: SecCNG
ms.assetid: 0ce50187-6376-4e14-aaa8-ecc401c7a973
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BCRYPT_AUTH_TAG_LENGTHS_STRUCT, BCRYPT_AUTH_TAG_LENGTHS_STRUCT structure [Security], BCRYPT_KEY_LENGTHS_STRUCT, BCRYPT_KEY_LENGTHS_STRUCT structure [Security], bcrypt/BCRYPT_AUTH_TAG_LENGTHS_STRUCT, bcrypt/BCRYPT_KEY_LENGTHS_STRUCT, security.bcrypt_key_lengths_struct
ms.topic: struct
f1_keywords: 
 - "bcrypt/BCRYPT_KEY_LENGTHS_STRUCT"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_KEY_LENGTHS_STRUCT
targetos: Windows
req.typenames: BCRYPT_KEY_LENGTHS_STRUCT
req.redist: 
ms.custom: 19H1
---

# BCRYPT_KEY_LENGTHS_STRUCT structure


## -description


The <b>BCRYPT_KEY_LENGTHS_STRUCT</b> structure defines the range of key sizes that are supported by the provider. This structure is used with the <b>BCRYPT_KEY_LENGTHS</b> property.

This structure is also used with the <b>BCRYPT_AUTH_TAG_LENGTH</b> property to contain the minimum, maximum, and increment size of an authentication tag.


## -struct-fields




### -field dwMinLength

The minimum length, in bits, of a key.


### -field dwMaxLength

The maximum length, in bits, of a key.


### -field dwIncrement

The number of bits that the key size can be incremented between <b>dwMinLength</b> and <b>dwMaxLength</b>.


## -remarks



The key sizes are given in a range that is inclusive of the minimum and maximum values and are separated by the increment. For example, if the minimum key size is 8 bits, the maximum key size is 16 bits, and the increment is 2 bits, the provider would support key sizes of 8, 10, 12, 14, and 16 bits.



