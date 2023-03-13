---
UID: NF:rtworkq.RtwqBeginRegisterWorkQueueWithMMCSS
title: RtwqBeginRegisterWorkQueueWithMMCSS function (rtworkq.h)
description: Associates a work queue with a Multimedia Class Scheduler Service (MMCSS) task. (RtwqBeginRegisterWorkQueueWithMMCSS)
helpviewer_keywords: ["RtwqBeginRegisterWorkQueueWithMMCSS","RtwqBeginRegisterWorkQueueWithMMCSS function","base.rtwqbeginregisterworkqueuewithmmcss","rtworkq/RtwqBeginRegisterWorkQueueWithMMCSS"]
old-location: base\rtwqbeginregisterworkqueuewithmmcss.htm
tech.root: backup
ms.assetid: 3012EFE9-437A-4B60-98DD-7602CD9A9E76
ms.date: 12/05/2018
ms.keywords: RtwqBeginRegisterWorkQueueWithMMCSS, RtwqBeginRegisterWorkQueueWithMMCSS function, base.rtwqbeginregisterworkqueuewithmmcss, rtworkq/RtwqBeginRegisterWorkQueueWithMMCSS
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
 - RtwqBeginRegisterWorkQueueWithMMCSS
 - rtworkq/RtwqBeginRegisterWorkQueueWithMMCSS
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
 - RtwqBeginRegisterWorkQueueWithMMCSS
---

# RtwqBeginRegisterWorkQueueWithMMCSS function


## -description

Associates a work queue with a Multimedia Class Scheduler Service (MMCSS) task.

## -parameters

### -param workQueueId [in]

The identifier of the work queue.  For private work queues, the identifier is returned by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a> function.

### -param usageClass [in]

The name of the MMCSS task.

### -param dwTaskId [in]

The unique task identifier. To obtain a new task identifier, set this value to zero.

### -param lPriority [in]

The base relative priority for the work-queue threads. For more information, see <a href="/windows/desktop/api/avrt/nf-avrt-avsetmmthreadpriority">AvSetMmThreadPriority</a>.

### -param doneCallback [in]

A pointer to the <a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasynccallback">IRtwqAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param doneState [in]

A pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
