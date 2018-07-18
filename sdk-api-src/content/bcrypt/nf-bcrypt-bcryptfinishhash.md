---
UID: NF:bcrypt.BCryptFinishHash
title: BCryptFinishHash function
author: windows-sdk-content
description: Retrieves the hash or Message Authentication Code (MAC) value for the data accumulated from prior calls to BCryptHashData.
old-location: security\bcryptfinishhash_func.htm
old-project: seccng
ms.assetid: 82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: BCryptFinishHash, BCryptFinishHash function [Security], bcrypt/BCryptFinishHash, security.bcryptfinishhash_func
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: HASHALGORITHM_ENUM
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
product: Windows
targetos: Windows
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
---

# BCryptFinishHash function


## -description


The <b>BCryptFinishHash</b> function retrieves the hash or <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Message Authentication Code</a> (MAC) value for the data accumulated from prior calls to <a href="https://msdn.microsoft.com/dab89dff-dc84-4f69-8b6b-de65704b0265">BCryptHashData</a>.


## -parameters




### -param hHash [in, out]

The handle of the hash or MAC object to use to compute the hash or MAC. This handle is obtained by calling the <a href="https://msdn.microsoft.com/deb02f67-f3d3-4542-8245-fd4982c3190b">BCryptCreateHash</a> function. After this function has been called, the hash handle passed to this function cannot be used again except in a call to <a href="https://msdn.microsoft.com/067dac61-98b9-478c-ac4d-e141961865e9">BCryptDestroyHash</a>.


### -param pbOutput [out]

A pointer to a buffer that receives the hash or MAC value. The <i>cbOutput</i> parameter contains the size of this buffer.


### -param cbOutput [in]

The size, in bytes, of the <i>pbOutput</i> buffer. This size must exactly match the size of the hash or MAC value.

The size can be obtained by calling the <a href="https://msdn.microsoft.com/5c62ca3a-843e-41a7-9340-41785fbb15f4">BCryptGetProperty</a> function to get the <b>BCRYPT_HASH_LENGTH</b> property. This will provide the size of the hash or MAC value for the specified algorithm.


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
The hash handle in the <i>hHash</i> parameter is not valid. After the <a href="https://msdn.microsoft.com/82a7c3d9-c01b-46d0-8b54-694dc0d8ffdd">BCryptFinishHash</a> function has been called for a hash  handle, that handle cannot be reused.

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



Depending on what processor modes a provider supports, <b>BCryptFinishHash</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/library/windows/hardware/ff551779">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hHash</i> parameter must be derived from an algorithm handle returned by a provider that was opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptFinishHash</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84080">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.






## -see-also




<a href="https://msdn.microsoft.com/dab89dff-dc84-4f69-8b6b-de65704b0265">BCryptHashData</a>
 

 

