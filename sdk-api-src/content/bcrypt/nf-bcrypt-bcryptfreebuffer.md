---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

