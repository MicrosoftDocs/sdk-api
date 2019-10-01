---
UID: NS:dispatcherqueue.DispatcherQueueOptions
title: DispatcherQueueOptions (dispatcherqueue.h)
author: windows-sdk-content
description: Specifies the threading and apartment type for a new DispatcherQueueController.
old-location: base\dispatcherqueueoptions.htm
tech.root: ProcThread
ms.assetid: F9AF7DDE-13EB-43DB-BAD5-61A6ABD9307D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DispatcherQueueOptions, DispatcherQueueOptions structure, base.dispatcherqueueoptions, dispatcherqueue/DispatcherQueueOptions
ms.topic: struct
f1_keywords: 
 - "dispatcherqueue/DispatcherQueueOptions"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/dispatcherqueue/nf-dispatcherqueue-createdispatcherqueuecontroller">CreateDispatcherQueueController</a>
 

 

