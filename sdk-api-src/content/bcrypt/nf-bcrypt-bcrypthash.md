---
UID: NF:bcrypt.BCryptHash
title: BCryptHash function (bcrypt.h)
description: Performs a single hash or MAC computation. This is a convenience function that wraps calls to BCryptCreateHash, BCryptHashData, BCryptFinishHash, and BCryptDestroyHash.
helpviewer_keywords: ["BCryptHash","BCryptHash function [Security]","bcrypt/BCryptHash","security.bcrypthash"]
old-location: security\bcrypthash.htm
tech.root: security
ms.assetid: F0FF9B6D-1345-480A-BE13-BE90547407BF
ms.date: 07/01/2025
ms.keywords: BCryptHash, BCryptHash function [Security], bcrypt/BCryptHash, security.bcrypthash
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptHash
 - bcrypt/BCryptHash
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - bcrypt.dll
api_name:
 - BCryptHash
---

# BCryptHash function


## -description

Performs a single cryptographic hash or [Message Authentication Code](/windows/win32/SecGloss/m-gly) (MAC) computation. This is a convenience function that wraps calls to [BCryptCreateHash](nf-bcrypt-bcryptcreatehash.md), [BCryptHashData](nf-bcrypt-bcrypthashdata.md), [BCryptFinishHash](nf-bcrypt-bcryptfinishhash.md), and [BCryptDestroyHash](nf-bcrypt-bcryptdestroyhash.md).

## -parameters

### -param hAlgorithm [in, out]

The handle of an algorithm provider that supports the hash or MAC interface. This handle is obtained by calling the [BCryptOpenAlgorithmProvider](nf-bcrypt-bcryptopenalgorithmprovider.md) function, or may be a [CNG Algorithm Pseudo-handle](/windows/win32/seccng/cng-algorithm-pseudo-handles).

### -param pbSecret [in, optional]

A pointer to a buffer that contains the key to use for a MAC. The *cbSecret* parameter contains the size of this buffer. If used with a hash algorithm, the algorithm must have been promoted to HMAC by using the **BCRYPT_ALG_HANDLE_HMAC** flag in [BCryptOpenAlgorithmProvider](nf-bcrypt-bcryptopenalgorithmprovider.md).

To compute a hash, set this parameter to `NULL`.

### -param cbSecret [in]

The size, in bytes, of the *pbSecret* buffer. If no key is used, set this parameter to zero.

### -param pbInput [in]

A pointer to a buffer that contains the data to process. The *cbInput* parameter contains the number of bytes in this buffer. This function does not modify the contents of this buffer.

### -param cbInput [in]

The size, in bytes, of the *pbInput* buffer.

### -param pbOutput [out]

A pointer to a buffer that receives the hash or MAC value. The <i>cbOutput</i> parameter contains the size of this buffer.

### -param cbOutput [in]

The size, in bytes, of the *pbOutput* buffer. This size must exactly match the size of the hash or MAC value if it has a fixed size.

The size can be obtained by calling the [BCryptGetProperty](nf-bcrypt-bcryptgetproperty.md) function to get the **BCRYPT_HASH_LENGTH** property. This will provide the size of the hash or MAC value for the specified algorithm. Extendable-output functions (XOFs), such as SHAKE256 may support a variable output size, but a default size which maintains full security of the XOF can be queried using **BCRYPT_HASH_LENGTH**.

## -returns

A status code indicating success or failure.

## -see-also

[BCryptCreateHash](nf-bcrypt-bcryptcreatehash.md)

[BCryptHashData](nf-bcrypt-bcrypthashdata.md)

[BCryptFinishHash](nf-bcrypt-bcryptfinishhash.md)

[BCryptDestroyHash](nf-bcrypt-bcryptdestroyhash.md)
