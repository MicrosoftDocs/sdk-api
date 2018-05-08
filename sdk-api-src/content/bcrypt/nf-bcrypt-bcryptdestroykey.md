---
UID: NF:bcrypt.BCryptDestroyKey
title: BCryptDestroyKey function
author: windows-driver-content
description: Destroys a key.
old-location: security\bcryptdestroykey_func.htm
old-project: SecCNG
ms.assetid: 98c02e55-6489-4901-8a7a-021baac41965
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: BCryptDestroyKey, BCryptDestroyKey function [Security], bcrypt/BCryptDestroyKey, security.bcryptdestroykey_func
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
-	BCryptDestroyKey
product: Windows
targetos: Windows
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
---

# BCryptDestroyKey function


## -description


The <b>BCryptDestroyKey</b> function destroys a key.


## -parameters




### -param hKey [in, out]

The handle of the key to destroy.


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
The key handle in the <i>hKey</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



Depending on what processor modes a provider supports, <b>BCryptDestroyKey</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/library/windows/hardware/ff551779">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hKey</i> parameter must be derived from an algorithm handle returned by a provider that was opened with the <b>BCRYPT_PROV_DISPATCH</b> flag.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84080">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.






## -see-also




<a href="https://msdn.microsoft.com/cdf0de2e-2445-45e3-91ba-89791a0c0642">BCryptGenerateKeyPair</a>



<a href="https://msdn.microsoft.com/c55d714f-f47e-4ddf-97b9-985c0441bb2d">BCryptGenerateSymmetricKey</a>



<a href="https://msdn.microsoft.com/6b9683f4-10f2-40e4-9757-a1f01991bef7">BCryptImportKey</a>



<a href="https://msdn.microsoft.com/271fc084-6121-4666-b521-b849c7d7966c">BCryptImportKeyPair</a>
 

 

