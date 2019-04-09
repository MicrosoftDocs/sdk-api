---
UID: NE:bcrypt.__unnamed_enum_4
title: BCRYPT_HASH_OPERATION_TYPE (bcrypt.h)
author: windows-sdk-content
description: The BCRYPT_HASH_OPERATION_TYPE enumeration specifies the hash operation type.
old-location: security\bcrypt_hash_operation_type.htm
tech.root: SecCNG
ms.assetid: DC570FB0-15DF-442C-951A-52A3120DB782
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BCRYPT_HASH_OPERATION_FINISH_HASH, BCRYPT_HASH_OPERATION_HASH_DATA, BCRYPT_HASH_OPERATION_TYPE, BCRYPT_HASH_OPERATION_TYPE enumeration [Security], bcrypt/BCRYPT_HASH_OPERATION_FINISH_HASH, bcrypt/BCRYPT_HASH_OPERATION_HASH_DATA, bcrypt/BCRYPT_HASH_OPERATION_TYPE, security.bcrypt_hash_operation_type
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: BCRYPT_HASH_OPERATION_TYPE
req.redist: 
---

# BCRYPT_HASH_OPERATION_TYPE enumeration


## -description


The <b>BCRYPT_HASH_OPERATION_TYPE</b> enumeration specifies the hash operation type.


## -enum-fields




### -field BCRYPT_HASH_OPERATION_HASH_DATA

Equivalent to calling the <a href="https://msdn.microsoft.com/dab89dff-dc84-4f69-8b6b-de65704b0265">BCryptHashData</a> function.


### -field BCRYPT_HASH_OPERATION_FINISH_HASH

Equivalent to calling the <a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a> function.


## -see-also




<a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a>



<a href="https://msdn.microsoft.com/dab89dff-dc84-4f69-8b6b-de65704b0265">BCryptHashData</a>
 

 

