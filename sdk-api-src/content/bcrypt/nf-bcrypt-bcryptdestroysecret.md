---
UID: NF:bcrypt.BCryptDestroySecret
title: BCryptDestroySecret function
author: windows-sdk-content
description: Destroys a secret agreement handle that was created by using the BCryptSecretAgreement function.
old-location: security\bcryptdestroysecret.htm
old-project: SecCNG
ms.assetid: 237743ff-ecb1-4c01-b4f9-192f27716f2c
ms.author: windowssdkdev
ms.date: 05/01/2018
ms.keywords: BCryptDestroySecret, BCryptDestroySecret function [Security], bcrypt/BCryptDestroySecret, security.bcryptdestroysecret
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	BCryptDestroySecret
product: Windows
targetos: Windows
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
---

# BCryptDestroySecret function


## -description


The <b>BCryptDestroySecret</b> function destroys a secret agreement handle that was created by using the <a href="https://msdn.microsoft.com/96863d81-3643-4962-8abf-db1cc2acde07">BCryptSecretAgreement</a> function.


## -parameters




### -param hSecret [in]

The <b>BCRYPT_SECRET_HANDLE</b> to be destroyed.


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
The handle in the <i>hSecret</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



Depending on what processor modes a provider supports, <b>BCryptDestroySecret</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/library/windows/hardware/ff551779">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hSecret</i> parameter must be derived from an algorithm handle returned by a provider that was opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84080">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.






## -see-also




<a href="https://msdn.microsoft.com/96863d81-3643-4962-8abf-db1cc2acde07">BCryptSecretAgreement</a>
 

 

