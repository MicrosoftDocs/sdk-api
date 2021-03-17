---
UID: NF:bcrypt.BCryptFinishHash
title: BCryptFinishHash function (bcrypt.h)
description: Retrieves the hash or Message Authentication Code (MAC) value for the data accumulated from prior calls to BCryptHashData.
helpviewer_keywords: ["BCryptFinishHash","BCryptFinishHash function [Security]","bcrypt/BCryptFinishHash","security.bcryptfinishhash_func"]
old-location: security\bcryptfinishhash_func.htm
tech.root: security
ms.assetid: 82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd
ms.date: 12/05/2018
ms.keywords: BCryptFinishHash, BCryptFinishHash function [Security], bcrypt/BCryptFinishHash, security.bcryptfinishhash_func
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
 - BCryptFinishHash
 - bcrypt/BCryptFinishHash
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
 - BCryptFinishHash
---

# BCryptFinishHash function


## -description

The <b>BCryptFinishHash</b> function retrieves the hash or <a href="/windows/desktop/SecGloss/m-gly">Message Authentication Code</a> (MAC) value for the data accumulated from prior calls to <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcrypthashdata">BCryptHashData</a>.

## -parameters

### -param hHash [in, out]

The handle of the hash or MAC object to use to compute the hash or MAC. This handle is obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptcreatehash">BCryptCreateHash</a> function. After this function has been called, the hash handle passed to this function cannot be used again except in a call to <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroyhash">BCryptDestroyHash</a>.

### -param pbOutput [out]

A pointer to a buffer that receives the hash or MAC value. The <i>cbOutput</i> parameter contains the size of this buffer.

### -param cbOutput [in]

The size, in bytes, of the <i>pbOutput</i> buffer. This size must exactly match the size of the hash or MAC value.

The size can be obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a> function to get the <b>BCRYPT_HASH_LENGTH</b> property. This will provide the size of the hash or MAC value for the specified algorithm.

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
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The hash handle in the <i>hHash</i> parameter is not valid. After the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a> function has been called for a hash  handle, that handle cannot be reused.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid. This includes the case where <i>cbOutput</i> is not the same size as the hash.

</td>
</tr>
</table>

## -remarks

Depending on what processor modes a provider supports, <b>BCryptFinishHash</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hHash</i> parameter must be derived from an algorithm handle returned by a provider that was opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptFinishHash</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcrypthashdata">BCryptHashData</a>