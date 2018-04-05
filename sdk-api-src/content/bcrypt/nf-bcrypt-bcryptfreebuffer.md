---
UID: NF:bcrypt.BCryptFreeBuffer
title: BCryptFreeBuffer function
author: windows-driver-content
description: Used to free memory that was allocated by one of the CNG functions.
old-location: security\bcryptfreebuffer_func.htm
old-project: SecCNG
ms.assetid: 0ee83ca1-2fe6-4ff2-823e-888b3e66f310
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: BCryptFreeBuffer, BCryptFreeBuffer function [Security], bcrypt/BCryptFreeBuffer, security.bcryptfreebuffer_func
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
-	BCryptFreeBuffer
product: Windows
targetos: Windows
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
---

# BCryptFreeBuffer function


## -description


The <b>BCryptFreeBuffer</b> function is used to free memory that was allocated by one of the CNG functions.


## -parameters




### -param pvBuffer [in]

A pointer to the memory buffer to be freed.


## -returns



This function does not return a value.




## -remarks




<b>BCryptFreeBuffer</b> must be called in the same processor mode as the BCrypt API function that allocated the buffer. In addition, if the buffer was allocated at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/library/windows/hardware/ff551779">IRQL</a>, it must be freed at that <i>IRQL</i>. If the buffer was allocated at <b>DISPATCH_LEVEL</b> <i>IRQL</i>, it can be freed at either <b>DISPATCH_LEVEL</b> <i>IRQL</i> or <b>PASSIVE_LEVEL</b> <i>IRQL</i>.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84080">WDK and Developer Tools</a>.<b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.






## -see-also




<a href="https://msdn.microsoft.com/02646a80-6e93-4169-83da-0488ff3da56f">BCryptEnumContexts</a>



<a href="https://msdn.microsoft.com/a01adfec-dbe0-4817-af97-63163760fafc">BCryptEnumRegisteredProviders</a>



<a href="https://msdn.microsoft.com/28b8bca9-442f-4d58-86aa-8aa274777ede">BCryptQueryProviderRegistration</a>
 

 

