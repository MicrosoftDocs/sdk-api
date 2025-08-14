---
UID: NF:bcrypt.BCryptDuplicateKey
title: BCryptDuplicateKey function (bcrypt.h)
description: Creates a duplicate of a symmetric key.
helpviewer_keywords: ["BCryptDuplicateKey","BCryptDuplicateKey function [Security]","bcrypt/BCryptDuplicateKey","security.bcryptduplicatekey_func"]
old-location: security\bcryptduplicatekey_func.htm
tech.root: security
ms.assetid: 13a0b904-353f-498a-bdc2-2fd4e51144ff
ms.date: 12/05/2018
ms.keywords: BCryptDuplicateKey, BCryptDuplicateKey function [Security], bcrypt/BCryptDuplicateKey, security.bcryptduplicatekey_func
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
 - BCryptDuplicateKey
 - bcrypt/BCryptDuplicateKey
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
 - BCryptDuplicateKey
---

# BCryptDuplicateKey function


## -description

The <b>BCryptDuplicateKey</b> function creates a duplicate of a <a href="/windows/desktop/SecGloss/s-gly">symmetric key</a>.

## -parameters

### -param hKey [in]

The handle of the key to duplicate. This must be a handle to a symmetric key.

### -param phNewKey [out]

A pointer to a <b>BCRYPT_KEY_HANDLE</b> variable that receives the handle of the duplicate key. This handle is used in subsequent functions that require a key, such as <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a>. This handle must be released when it is no longer needed by passing it to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a> function.

### -param pbKeyObject [out]

An ***optional*** pointer to a buffer that receives the duplicate key object. The <i>cbKeyObject</i> parameter contains the size of this buffer. The required size of this buffer can be obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a> function to get the <b>BCRYPT_OBJECT_LENGTH</b> property. This will provide the size of the key object for the specified algorithm.

This memory can only be freed after the <i>phNewKey</i> key handle is destroyed.

If the value of this parameter is <b>NULL</b> and the value of the <i>cbKeyObject</i> parameter is zero, the memory for the duplicate key object is allocated by this function and freed by <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a>. <b>Windows 7:  </b>This memory management functionality is available beginning with Windows 7.

### -param cbKeyObject [in]

The size, in bytes, of the <i>pbKeyObject</i> buffer.

If the value of this parameter is zero and the value of the <i>pbKeyObject</i> parameter is <b>NULL</b>, the memory for the duplicate key object is allocated by this function and freed by <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a>. <b>Windows 7:  </b>This memory management functionality is available beginning with Windows 7.

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
The size of the key object specified by the <i>cbKeyObject</i> parameter is not large enough to hold the key object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The key handle in the <i>hKey</i> parameter is not valid. This value is also returned if the key to duplicate is not a symmetric key.

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

When using a supported algorithm provider, <b>BCryptDuplicateKey</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hKey</i> parameter must be derived from an algorithm handle returned by a provider that was opened with the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptDuplicateKey</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.
