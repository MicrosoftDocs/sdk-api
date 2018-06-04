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

# RtwqLockSharedWorkQueue function


## -description


Obtains and locks a shared work queue.


## -parameters




### -param usageClass [in]

The name of the Multimedia Class Scheduler Service (MMCSS) task. 


### -param basePriority [in]

The base priority of the work-queue threads. If the regular-priority queue is being used (<code>usageClass=""</code>), then the value 0 must be passed in.


### -param taskId [in, out]

The MMCSS task identifier. On input, specify an existing MCCSS task group ID, or use the value zero to create a new task group. If the regular priority queue is being used (<code>usageClass=""</code>), then <b>NULL</b> must be passed in. On output, receives the actual task group ID.


### -param id

TBD




#### - pID [out]

Receives an identifier for the new work queue. Use this identifier when queuing work items.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



