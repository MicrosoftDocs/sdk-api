---
UID: NF:bcrypt.BCryptHashData
title: BCryptHashData function (bcrypt.h)
description: Performs a one way hash or Message Authentication Code (MAC) on a data buffer.
helpviewer_keywords: ["BCryptHashData","BCryptHashData function [Security]","bcrypt/BCryptHashData","security.bcrypthashdata_func"]
old-location: security\bcrypthashdata_func.htm
tech.root: security
ms.assetid: dab89dff-dc84-4f69-8b6b-de65704b0265
ms.date: 12/05/2018
ms.keywords: BCryptHashData, BCryptHashData function [Security], bcrypt/BCryptHashData, security.bcrypthashdata_func
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
 - BCryptHashData
 - bcrypt/BCryptHashData
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
 - BCryptHashData
---

# BCryptHashData function


## -description

The <b>BCryptHashData</b> function performs a one way hash or <a href="/windows/desktop/SecGloss/m-gly">Message Authentication Code</a> (MAC) on a data buffer.

## -parameters

### -param hHash [in, out]

The handle of the hash or MAC object to use to perform the operation. This handle is obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptcreatehash">BCryptCreateHash</a> function.

### -param pbInput [in]

A pointer to a buffer that contains the data to process. The <i>cbInput</i> parameter contains the number of bytes in this buffer. This function does not modify the contents of this buffer.

### -param cbInput [in]

The number of bytes in the <i>pbInput</i> buffer.

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
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

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
</table>

## -remarks

To combine more than one buffer into the hash or MAC, you can call this function multiple times, passing a different buffer each time. To obtain the hash or MAC value, call the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a> function. After the <b>BCryptFinishHash</b> function has been called for a specified  handle, that handle cannot be reused.

Depending on what processor modes a provider supports, <b>BCryptHashData</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hHash</i> parameter must be derived from an algorithm handle returned by a provider that was opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptHashData</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptcreatehash">BCryptCreateHash</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptfinishhash">BCryptFinishHash</a>