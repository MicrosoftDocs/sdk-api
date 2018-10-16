---
UID: NF:avrt.AvRevertMmThreadCharacteristics
title: AvRevertMmThreadCharacteristics function
author: windows-sdk-content
description: Indicates that a thread is no longer performing work associated with the specified task.
old-location: base\avrevertmmthreadcharacteristics.htm
tech.root: procthread
ms.assetid: 2ae0d34c-3819-46fa-9779-5de8a57e5281
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: AvRevertMmThreadCharacteristics, AvRevertMmThreadCharacteristics function, avrt/AvRevertMmThreadCharacteristics, base.avrevertmmthreadcharacteristics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: avrt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Avrt.lib
req.dll: Avrt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvRevertMmThreadCharacteristics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AvRevertMmThreadCharacteristics function


## -description


Indicates that a thread is no longer performing work associated with the specified task.


## -parameters




### -param AvrtHandle [in]

A handle to the task. This handle is returned by the <a href="https://msdn.microsoft.com/881d3f97-e68e-40cb-b799-76784185dd37">AvSetMmThreadCharacteristics</a> or <a href="https://msdn.microsoft.com/d8137b53-b1fd-4c25-909a-d0ed671848df">AvSetMmMaxThreadCharacteristics</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function must be called from the same thread that called the <a href="https://msdn.microsoft.com/881d3f97-e68e-40cb-b799-76784185dd37">AvSetMmThreadCharacteristics</a> or <a href="https://msdn.microsoft.com/d8137b53-b1fd-4c25-909a-d0ed671848df">AvSetMmMaxThreadCharacteristics</a> function to create the handle. Otherwise, the function will fail.




## -see-also




<a href="https://msdn.microsoft.com/a7169938-1c72-4c4c-881a-cb08ad6182c7">Multimedia Class Scheduler Service</a>
 

 

