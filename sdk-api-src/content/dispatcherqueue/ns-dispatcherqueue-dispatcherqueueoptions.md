---
UID: NS:dispatcherqueue.DispatcherQueueOptions
title: DispatcherQueueOptions (dispatcherqueue.h)
description: Represents options around threading affinity and type of COM apartment for a new DispatcherQueueController.
helpviewer_keywords: ["DispatcherQueueOptions","DispatcherQueueOptions structure","base.dispatcherqueueoptions","dispatcherqueue/DispatcherQueueOptions"]
old-location: base\dispatcherqueueoptions.htm
tech.root: backup
ms.assetid: F9AF7DDE-13EB-43DB-BAD5-61A6ABD9307D
ms.date: 12/05/2018
ms.keywords: DispatcherQueueOptions, DispatcherQueueOptions structure, base.dispatcherqueueoptions, dispatcherqueue/DispatcherQueueOptions
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DispatcherQueueOptions
 - dispatcherqueue/DispatcherQueueOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DispatcherQueue.h
api_name:
 - DispatcherQueueOptions
---

## -description

Represents options around threading affinity and type of COM apartment for a new <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>.

## -struct-fields

### -field dwSize

Size of this <b>DispatcherQueueOptions</b> structure.

### -field threadType

Thread affinity for a new <a href="/uwp/api/windows.system.dispatcherqueuecontroller">DispatcherQueueController</a>.

### -field apartmentType

Specifies whether to initialize the COM apartment on the new thread as an application single-threaded apartment (ASTA) or a single-threaded apartment (STA). This field is relevant only if <b>threadType</b> is <b>DQTYPE_THREAD_DEDICATED</b>. Use <b>DQTAT_COM_NONE</b> when <b>DispatcherQueueOptions.threadType</b> is <b>DQTYPE_THREAD_CURRENT</b>.

## -remarks

Introduced in Windows 10, version 1709.

## -see-also

<a href="/windows/desktop/api/dispatcherqueue/nf-dispatcherqueue-createdispatcherqueuecontroller">CreateDispatcherQueueController</a>
