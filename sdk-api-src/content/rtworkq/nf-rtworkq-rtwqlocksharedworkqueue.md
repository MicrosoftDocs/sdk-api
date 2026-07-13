---
UID: NF:rtworkq.RtwqLockSharedWorkQueue
title: RtwqLockSharedWorkQueue function (rtworkq.h)
description: Obtains and locks a shared work queue. (RtwqLockSharedWorkQueue)
helpviewer_keywords: ["RtwqLockSharedWorkQueue","RtwqLockSharedWorkQueue function","base.rtwqlocksharedworkqueue","rtworkq/RtwqLockSharedWorkQueue"]
old-location: base\rtwqlocksharedworkqueue.htm
tech.root: backup
ms.assetid: ccebdbd8-fd3e-4e99-b1dd-1ec8e57cbff6
ms.date: 12/05/2018
ms.keywords: RtwqLockSharedWorkQueue, RtwqLockSharedWorkQueue function, base.rtwqlocksharedworkqueue, rtworkq/RtwqLockSharedWorkQueue
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtwqLockSharedWorkQueue
 - rtworkq/RtwqLockSharedWorkQueue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqLockSharedWorkQueue
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

### -param id [out]

Receives an identifier for the new work queue. Use this identifier when queuing work items.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

