---
UID: NF:bcrypt.BCryptGenerateSymmetricKey
title: BCryptGenerateSymmetricKey function (bcrypt.h)
description: Creates a key object for use with a symmetrical key encryption algorithm from a supplied key.
helpviewer_keywords: ["BCryptGenerateSymmetricKey","BCryptGenerateSymmetricKey function [Security]","bcrypt/BCryptGenerateSymmetricKey","security.bcryptgeneratesymmetrickey_func"]
old-location: security\bcryptgeneratesymmetrickey_func.htm
tech.root: security
ms.assetid: c55d714f-f47e-4ddf-97b9-985c0441bb2d
ms.date: 12/05/2018
ms.keywords: BCryptGenerateSymmetricKey, BCryptGenerateSymmetricKey function [Security], bcrypt/BCryptGenerateSymmetricKey, security.bcryptgeneratesymmetrickey_func
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
 - BCryptGenerateSymmetricKey
 - bcrypt/BCryptGenerateSymmetricKey
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
 - BCryptGenerateSymmetricKey
---

# BCryptGenerateSymmetricKey function


## -description

The <b>BCryptGenerateSymmetricKey</b> function creates a key object for use with  a symmetrical key encryption algorithm from a supplied key.

## -parameters

### -param hAlgorithm [in, out]

The handle of an algorithm provider created with the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a> function. The algorithm specified when the provider was created must support symmetric key encryption.

### -param phKey [out]

A pointer to a <b>BCRYPT_KEY_HANDLE</b> that receives the handle of the key. This handle is used in subsequent functions that require a key, such as <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a>. This handle must be released when it is no longer needed by passing it to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a> function.

### -param pbKeyObject [out, optional]

A pointer to a buffer that receives the key object. The <i>cbKeyObject</i> parameter contains the size of this buffer. The required size of this buffer can be obtained by calling the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a> function to get the <b>BCRYPT_OBJECT_LENGTH</b> property. This will provide the size of the key object for the specified algorithm.

This memory can only be freed after the <i>phKey</i> key handle is destroyed.

If the value of this parameter is <b>NULL</b> and the value of the <i>cbKeyObject</i> parameter is zero, the memory for the key object is allocated and freed by this function.<b>Windows 7:  </b>This memory management functionality is available beginning with Windows 7.

### -param cbKeyObject [in]

The size, in bytes, of the <i>pbKeyObject</i> buffer.

If the value of this parameter is zero and the value of the <i>pbKeyObject</i> parameter is <b>NULL</b>, the memory for the key object is allocated and freed by this function.<b>Windows 7:  </b>This memory management functionality is available beginning with Windows 7.

### -param pbSecret [in]

Pointer to a buffer that contains the key from which to create the key object. The <i>cbSecret</i> parameter contains the size of this buffer. This is normally a hash of a password or some other reproducible data. If the data passed in exceeds the target key size, the data will be truncated and the excess will be ignored.

<div class="alert"><b>Note</b>  We strongly recommended that applications pass in the exact number of bytes required by the target key.</div>
<div> </div>

### -param cbSecret [in]

The size, in bytes, of the <i>pbSecret</i> buffer.

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
The algorithm handle in the <i>hAlgorithm</i> parameter is not valid.

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

Depending on what processor modes a provider supports, <b>BCryptGenerateSymmetricKey</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hAlgorithm</i> parameter must have been opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptGenerateSymmetricKey</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroykey">BCryptDestroyKey</a>