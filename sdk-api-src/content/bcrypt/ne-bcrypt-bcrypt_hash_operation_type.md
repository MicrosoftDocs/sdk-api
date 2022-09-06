---
UID: NE:bcrypt.__unnamed_enum_4
title: BCRYPT_HASH_OPERATION_TYPE (bcrypt.h)
description: The BCRYPT_HASH_OPERATION_TYPE enumeration specifies the hash operation type.
helpviewer_keywords: ["BCRYPT_HASH_OPERATION_FINISH_HASH","BCRYPT_HASH_OPERATION_HASH_DATA","BCRYPT_HASH_OPERATION_TYPE","BCRYPT_HASH_OPERATION_TYPE enumeration [Security]","bcrypt/BCRYPT_HASH_OPERATION_FINISH_HASH","bcrypt/BCRYPT_HASH_OPERATION_HASH_DATA","bcrypt/BCRYPT_HASH_OPERATION_TYPE","security.bcrypt_hash_operation_type"]
old-location: security\bcrypt_hash_operation_type.htm
tech.root: security
ms.assetid: DC570FB0-15DF-442C-951A-52A3120DB782
ms.date: 12/05/2018
ms.keywords: BCRYPT_HASH_OPERATION_FINISH_HASH, BCRYPT_HASH_OPERATION_HASH_DATA, BCRYPT_HASH_OPERATION_TYPE, BCRYPT_HASH_OPERATION_TYPE enumeration [Security], bcrypt/BCRYPT_HASH_OPERATION_FINISH_HASH, bcrypt/BCRYPT_HASH_OPERATION_HASH_DATA, bcrypt/BCRYPT_HASH_OPERATION_TYPE, security.bcrypt_hash_operation_type
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
targetos: Windows
req.typenames: BCRYPT_HASH_OPERATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCRYPT_HASH_OPERATION_TYPE
 - bcrypt/BCRYPT_HASH_OPERATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - BCRYPT_HASH_OPERATION_TYPE
---

# BCRYPT_HASH_OPERATION_TYPE enumeration


## -description

The <b>BCRYPT_HASH_OPERATION_TYPE</b> enumeration specifies the hash operation type.

## -enum-fields

### -field BCRYPT_HASH_OPERATION_HASH_DATA:1

Equivalent to calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcrypthashdata">BCryptHashData</a> function.

### -field BCRYPT_HASH_OPERATION_FINISH_HASH:2

Equivalent to calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a> function.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcrypthashdata">BCryptHashData</a>
