---
UID: NF:bcrypt.BCryptHash
title: BCryptHash function (bcrypt.h)
description: Performs a single hash computation. This is a convenience function that wraps calls to BCryptCreateHash, BCryptHashData, BCryptFinishHash, and BCryptDestroyHash.
helpviewer_keywords: ["BCryptHash","BCryptHash function [Security]","bcrypt/BCryptHash","security.bcrypthash"]
old-location: security\bcrypthash.htm
tech.root: security
ms.assetid: F0FF9B6D-1345-480A-BE13-BE90547407BF
ms.date: 12/05/2018
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

Performs a single hash computation. This is a convenience function that wraps calls to <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptcreatehash">BCryptCreateHash</a>, <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcrypthashdata">BCryptHashData</a>, <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a>, and <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroyhash">BCryptDestroyHash</a>.

## -parameters

### -param hAlgorithm

The handle of an algorithm provider created by using the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a> function. The algorithm that was specified when the provider was created must support the hash interface.

### -param pbSecret

 A pointer to a buffer that contains the key to use for the hash or MAC. The <i>cbSecret</i> parameter contains the size of this buffer. This key only applies to hash algorithms opened by the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a> function by using the <b>BCRYPT_ALG_HANDLE_HMAC</b> flag.  Otherwise, set this parameter to <b>NULL</b>

### -param cbSecret

The size, in bytes, of the <i>pbSecret</i> buffer. If no key is used, set this parameter to zero.

### -param pbInput

A pointer to a buffer that contains the data to process. The <i>cbInput</i> parameter contains the number of bytes in this buffer. This function does not modify the contents of this buffer.

### -param cbInput

The number of bytes in the <i>pbInput</i> buffer.

### -param pbOutput

A pointer to a buffer that receives the hash or MAC value. The <i>cbOutput</i> parameter contains the size of this buffer.

### -param cbOutput

The size, in bytes, of the <i>pbOutput</i> buffer. This size must exactly match the size of the hash or MAC value.

The size can be obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a> function to get the <b>BCRYPT_HASH_LENGTH</b> property. This will provide the size of the hash or MAC value for the specified algorithm.

## -returns

A status code indicating success or failure.