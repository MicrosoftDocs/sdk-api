---
UID: NF:bcrypt.BCryptDestroyHash
title: BCryptDestroyHash function (bcrypt.h)
description: Destroys a hash or Message Authentication Code (MAC) object.
helpviewer_keywords: ["BCryptDestroyHash","BCryptDestroyHash function [Security]","bcrypt/BCryptDestroyHash","security.bcryptdestroyhash_func"]
old-location: security\bcryptdestroyhash_func.htm
tech.root: security
ms.assetid: 067dac61-98b9-478c-ac4d-e141961865e9
ms.date: 12/05/2018
ms.keywords: BCryptDestroyHash, BCryptDestroyHash function [Security], bcrypt/BCryptDestroyHash, security.bcryptdestroyhash_func
f1_keywords:
- bcrypt/BCryptDestroyHash
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Bcrypt.dll
- Ksecdd.sys
api_name:
- BCryptDestroyHash
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BCryptDestroyHash function


## -description


The <b>BCryptDestroyHash</b> function destroys a hash or <a href="https://docs.microsoft.com/windows/desktop/SecGloss/m-gly">Message Authentication Code</a> (MAC) object.


## -parameters




### -param hHash [in, out]

The handle of the hash or MAC object to destroy. This handle is obtained by using the <a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptcreatehash">BCryptCreateHash</a> function.


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
The algorithm handle in the <i>hHash</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



Depending on what processor modes a provider supports, <b>BCryptDestroyHash</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="https://docs.microsoft.com/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hHash</i> parameter must be derived from an algorithm handle returned by a provider that was opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bcrypt/nf-bcrypt-bcryptcreatehash">BCryptCreateHash</a>
 

 

