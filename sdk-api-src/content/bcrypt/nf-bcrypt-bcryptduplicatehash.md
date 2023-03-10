---
UID: NF:bcrypt.BCryptDuplicateHash
title: BCryptDuplicateHash function (bcrypt.h)
description: Duplicates an existing hash or Message Authentication Code (MAC) object.
helpviewer_keywords: ["BCryptDuplicateHash","BCryptDuplicateHash function [Security]","bcrypt/BCryptDuplicateHash","security.bcryptduplicatehash_func"]
old-location: security\bcryptduplicatehash_func.htm
tech.root: security
ms.assetid: 451ff5dc-b66a-4e8e-a327-28b4ee618b74
ms.date: 12/05/2018
ms.keywords: BCryptDuplicateHash, BCryptDuplicateHash function [Security], bcrypt/BCryptDuplicateHash, security.bcryptduplicatehash_func
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - BCryptDuplicateHash
 - bcrypt/BCryptDuplicateHash
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptDuplicateHash
---

# BCryptDuplicateHash function


## -description

The <b>BCryptDuplicateHash</b> function duplicates an existing hash or <a href="/windows/desktop/SecGloss/m-gly">Message Authentication Code</a> (MAC) object. The duplicate object contains all state and data contained in the original object at the point of duplication.

## -parameters

### -param hHash [in]

The handle of the hash or MAC object to duplicate.

### -param phNewHash [out]

A pointer to a <b>BCRYPT_HASH_HANDLE</b> value that receives the handle that represents the duplicate hash or MAC object.

### -param pbHashObject [out]

A pointer to a buffer that receives the duplicate hash or MAC object. The <i>cbHashObject</i> parameter contains the size of this buffer. The required size of this buffer can be obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a> function to get the <b>BCRYPT_OBJECT_LENGTH</b> property. This will provide the size of the hash object for the specified algorithm.

When the duplicate hash handle is released, free this memory.

### -param cbHashObject [in]

The size, in bytes, of the <i>pbHashObject</i> buffer.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are currently defined, so this parameter should be zero.

## -returns

Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The size of the hash object specified by the <i>cbHashObject</i> parameter is not large enough to hold the hash object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The hash handle in the <i>hHash</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
</table>

## -remarks

This function is useful when computing a hash or MAC over a block of common data. After the common data has been processed, the hash or MAC object can be duplicated, and then the unique data can be added to the individual objects.

Depending on what processor modes a provider supports, <b>BCryptDuplicateHash</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hHash</i> parameter must be derived from an algorithm handle returned by a provider that was opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.