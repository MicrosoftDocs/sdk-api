---
UID: NF:bcrypt.BCryptCreateHash
title: BCryptCreateHash function
author: windows-driver-content
description: Called to create a hash or Message Authentication Code (MAC) object.
old-location: security\bcryptcreatehash_func.htm
old-project: SecCNG
ms.assetid: deb02f67-f3d3-4542-8245-fd4982c3190b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: BCRYPT_HASH_REUSABLE_FLAG, BCryptCreateHash, BCryptCreateHash function [Security], bcrypt/BCryptCreateHash, security.bcryptcreatehash_func
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: HASHALGORITHM_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Bcrypt.dll
-	Ksecdd.sys
api_name:
-	BCryptCreateHash
product: Windows
targetos: Windows
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
---

# BCryptCreateHash function


## -description


The <b>BCryptCreateHash</b> function is called to create a hash or <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Message Authentication Code</a> (MAC) object.


## -parameters




### -param hAlgorithm [in, out]

The handle of an algorithm provider created by using the <a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a> function. The algorithm that was specified when the provider was created must support the hash interface.


### -param phHash [out]

A pointer to a <b>BCRYPT_HASH_HANDLE</b> value that receives a handle that represents the hash or MAC object. This handle is used in subsequent hashing or MAC functions, such as the <a href="https://msdn.microsoft.com/dab89dff-dc84-4f69-8b6b-de65704b0265">BCryptHashData</a> function. When you have finished using this handle, release it by passing it to the <a href="https://msdn.microsoft.com/067dac61-98b9-478c-ac4d-e141961865e9">BCryptDestroyHash</a> function.


### -param pbHashObject [out]

A pointer to a buffer that receives the hash or MAC object. The <i>cbHashObject</i> parameter contains the size of this buffer. The required size of this buffer can be obtained by calling the <a href="https://msdn.microsoft.com/5c62ca3a-843e-41a7-9340-41785fbb15f4">BCryptGetProperty</a> function to get the <b>BCRYPT_OBJECT_LENGTH</b> property. This will provide the size of the hash or MAC object for the specified algorithm.

This memory can only be freed after the handle pointed to by the <i>phHash</i> parameter is destroyed.

If the value of this parameter is <b>NULL</b> and the value of the <i>cbHashObject</i> parameter is zero, the memory for the hash object is allocated and freed by this function.<b>Windows 7:  </b>This memory management functionality is available beginning with Windows 7.




### -param cbHashObject [in, optional]

The size, in bytes, of the <i>pbHashObject</i> buffer.

If the value of this parameter is zero and the value of the <i>pbHashObject</i> parameter is <b>NULL</b>, the memory for the key object is allocated and freed by this function.<b>Windows 7:  </b>This memory management functionality is available beginning with Windows 7.</p>c


### -param pbSecret [in, optional]

A pointer to a buffer that contains the key to use for the hash or MAC. The <i>cbSecret</i> parameter contains the size of this buffer. This key only applies to hash algorithms opened by the <a href="https://msdn.microsoft.com/aceba9c0-19e6-4f3c-972a-752feed4a9f8">BCryptOpenAlgorithmProvider</a> function by using the <b>BCRYPT_ALG_HANDLE_HMAC</b> flag.  Otherwise, set this parameter to <b>NULL</b>.


### -param cbSecret [in]

The size, in bytes, of the <i>pbSecret</i> buffer. If no key is used, set this parameter to zero.


### -param dwFlags [in]

Flags that modify the behavior of the function. This can be zero or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BCRYPT_HASH_REUSABLE_FLAG"></a><a id="bcrypt_hash_reusable_flag"></a><dl>
<dt><b>BCRYPT_HASH_REUSABLE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Creates a reusable hashing object. The object can be used for a new hashing operation immediately after calling <a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a>. For more information, see <a href="https://msdn.microsoft.com/f36b7e36-4377-4940-8951-6caba6e3ce8a">Creating a Hash with CNG</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This flag is not supported.

</td>
</tr>
</table>
 


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
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The algorithm provider specified by the <i>hAlgorithm</i> parameter does not support the hash interface.

</td>
</tr>
</table>
 




## -remarks



Depending on what processor modes a provider supports, <b>BCryptCreateHash</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/library/windows/hardware/ff551779">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hAlgorithm</i> parameter must have been opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptCreateHash</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84080">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.






## -see-also




<a href="https://msdn.microsoft.com/067dac61-98b9-478c-ac4d-e141961865e9">BCryptDestroyHash</a>
 

 

