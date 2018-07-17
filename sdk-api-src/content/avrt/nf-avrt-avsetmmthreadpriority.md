---
UID: NF:avrt.AvSetMmThreadPriority
title: AvSetMmThreadPriority function
author: windows-sdk-content
description: Adjusts the thread priority of the calling thread relative to other threads performing the same task.
old-location: base\avsetmmthreadpriority.htm
old-project: procthread
ms.assetid: 74259dbc-a9e9-409e-96e6-66a9dc590099
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AVRT_PRIORITY_CRITICAL, AVRT_PRIORITY_HIGH, AVRT_PRIORITY_LOW, AVRT_PRIORITY_NORMAL, AvSetMmThreadPriority, AvSetMmThreadPriority function, avrt/AvSetMmThreadPriority, base.avsetmmthreadpriority
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AVRF_HEAP_ALLOCATION, *PAVRF_HEAP_ALLOCATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avrt.dll
api_name:
 - AvSetMmThreadPriority
product: Windows
targetos: Windows
req.lib: Avrt.lib
req.dll: Avrt.dll
req.irql: 
---

# AvSetMmThreadPriority function


## -description


Adjusts the thread priority of the calling thread relative to other threads performing the same task.


## -parameters




### -param AvrtHandle [in]

A handle to the task. This handle is returned by the <a href="https://msdn.microsoft.com/881d3f97-e68e-40cb-b799-76784185dd37">AvSetMmThreadCharacteristics</a> or <a href="https://msdn.microsoft.com/d8137b53-b1fd-4c25-909a-d0ed671848df">AvSetMmMaxThreadCharacteristics</a> function.


### -param Priority [in]

The relative thread priority of this thread to other threads performing a similar task. This parameter can be one of the following values.



#### AVRT_PRIORITY_CRITICAL (2)



#### AVRT_PRIORITY_HIGH (1)



#### AVRT_PRIORITY_LOW (-1)



#### AVRT_PRIORITY_NORMAL (0)


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/a7169938-1c72-4c4c-881a-cb08ad6182c7">Multimedia Class Scheduler Service</a>
 

 

