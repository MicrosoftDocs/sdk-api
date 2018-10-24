---
UID: NS:dispatcherqueue.DispatcherQueueOptions
title: DispatcherQueueOptions
author: windows-sdk-content
description: Specifies the threading and apartment type for a new DispatcherQueueController.
old-location: base\dispatcherqueueoptions.htm
tech.root: ProcThread
ms.assetid: F9AF7DDE-13EB-43DB-BAD5-61A6ABD9307D
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: DispatcherQueueOptions, DispatcherQueueOptions structure, base.dispatcherqueueoptions, dispatcherqueue/DispatcherQueueOptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dispatcherqueue.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DispatcherQueue.h
api_name:
 - DispatcherQueueOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DispatcherQueueOptions structure


## -description


Specifies the threading and apartment type for a new <a href="https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>.


## -struct-fields




### -field dwSize

Size of this <b>DispatcherQueueOptions</b> structure.


### -field threadType

Thread affinity for the created <a href="https://docs.microsoft.com/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>.


### -field apartmentType

Specifies whether to initialize COM apartment on the new thread as an application single-threaded apartment (ASTA)  or single-threaded apartment (STA). This field is only relevant if <b>threadType</b> is <b>DQTYPE_THREAD_DEDICATED</b>. Use <b>DQTAT_COM_NONE</b> when <b>DispatcherQueueOptions.threadType</b> is <b>DQTYPE_THREAD_CURRENT</b>.


## -remarks



Introduced in Windows 10, version 1709.




## -see-also




<a href="https://msdn.microsoft.com/750097BB-C4D1-4579-9353-582124D5CE3B">CreateDispatcherQueueController</a>
 

 

