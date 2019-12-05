---
UID: NE:bcrypt.__unnamed_enum_4
title: BCRYPT_HASH_OPERATION_TYPE (bcrypt.h)
description: The BCRYPT_HASH_OPERATION_TYPE enumeration specifies the hash operation type.
old-location: security\bcrypt_hash_operation_type.htm
tech.root: SecCNG
ms.assetid: DC570FB0-15DF-442C-951A-52A3120DB782
ms.date: 12/05/2018
ms.keywords: BCRYPT_HASH_OPERATION_FINISH_HASH, BCRYPT_HASH_OPERATION_HASH_DATA, BCRYPT_HASH_OPERATION_TYPE, BCRYPT_HASH_OPERATION_TYPE enumeration [Security], bcrypt/BCRYPT_HASH_OPERATION_FINISH_HASH, bcrypt/BCRYPT_HASH_OPERATION_HASH_DATA, bcrypt/BCRYPT_HASH_OPERATION_TYPE, security.bcrypt_hash_operation_type
ms.topic: enum
f1_keywords:
- bcrypt/BCRYPT_HASH_OPERATION_TYPE
dev_langs:
- c++
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
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
- BCRYPT_HASH_OPERATION_TYPE
targetos: Windows
req.typenames: BCRYPT_HASH_OPERATION_TYPE
req.redist: 
ms.custom: 19H1
---

# BCRYPT_HASH_OPERATION_TYPE enumeration


## -description


The <b>BCRYPT_HASH_OPERATION_TYPE</b> enumeration specifies the hash operation type.


## -enum-fields




### -field BCRYPT_HASH_OPERATION_HASH_DATA

Equivalent to calling the <a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcrypthashdata">BCryptHashData</a> function.


### -field BCRYPT_HASH_OPERATION_FINISH_HASH

Equivalent to calling the <a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a> function.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a>



<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcrypthashdata">BCryptHashData</a>
 

 

