---
UID: NS:bcrypt._BCRYPT_MULTI_HASH_OPERATION
title: BCRYPT_MULTI_HASH_OPERATION (bcrypt.h)
description: A BCRYPT_MULTI_HASH_OPERATION structure defines a single operation in a multi-hash operation.
helpviewer_keywords: ["BCRYPT_MULTI_HASH_OPERATION","BCRYPT_MULTI_HASH_OPERATION structure [Security]","bcrypt/BCRYPT_MULTI_HASH_OPERATION","security.bcrypt_multi_hash_operation"]
old-location: security\bcrypt_multi_hash_operation.htm
tech.root: security
ms.assetid: B0418A07-D2EE-4346-9971-676C8FB08FAA
ms.date: 12/05/2018
ms.keywords: BCRYPT_MULTI_HASH_OPERATION, BCRYPT_MULTI_HASH_OPERATION structure [Security], bcrypt/BCRYPT_MULTI_HASH_OPERATION, security.bcrypt_multi_hash_operation
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 Update [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 Update [desktop apps \| UWP apps]
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
req.typenames: BCRYPT_MULTI_HASH_OPERATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BCRYPT_MULTI_HASH_OPERATION
 - bcrypt/_BCRYPT_MULTI_HASH_OPERATION
 - BCRYPT_MULTI_HASH_OPERATION
 - bcrypt/BCRYPT_MULTI_HASH_OPERATION
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
 - BCRYPT_MULTI_HASH_OPERATION
---

# BCRYPT_MULTI_HASH_OPERATION structure


## -description

A <b>BCRYPT_MULTI_HASH_OPERATION</b> structure defines a single operation in a multi-hash operation.

## -struct-fields

### -field iHash

An index into the multi-object state array of the hash state on which this computation operates. The first element of the array corresponds to an <i>iHash</i> value of zero (0). Valid values are less than the value of the <i>nHashes</i> parameter of the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptcreatemultihash">BCryptCreateMultiHash</a> function.

### -field hashOperation

A hash operation type, either <b>BCRYPT_HASH_OPERATION_HASH_DATA</b> or <b>BCRYPT_HASH_OPERATION_FINISH_HASH</b>.

If the value is <b>BCRYPT_HASH_OPERATION_HASH_DATA</b>, the operation performed is  equivalent to calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcrypthashdata">BCryptHashData</a> function on the hash object array element with <i>pbBuffer</i>/<i>cbBuffer</i> pointing to the buffer to be hashed.

If the value is <b>BCRYPT_HASH_OPERATION_FINISH_HASH</b>, the operation performed is  equivalent to calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a> function on the hash object array element with <i>pbBuffer</i>/<i>cbBuffer</i> pointing to the output buffer that receives the result.

### -field pbBuffer

The buffer on which the operation works.

### -field cbBuffer

The buffer on which the operation works.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptcreatemultihash">BCryptCreateMultiHash</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcrypthashdata">BCryptHashData</a>