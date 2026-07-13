---
UID: NF:rtworkq.RtwqBeginUnregisterWorkQueueWithMMCSS
title: RtwqBeginUnregisterWorkQueueWithMMCSS function (rtworkq.h)
description: Unregisters a work queue from a Multimedia Class Scheduler Service (MMCSS) task. (RtwqBeginUnregisterWorkQueueWithMMCSS)
helpviewer_keywords: ["RtwqBeginUnregisterWorkQueueWithMMCSS","RtwqBeginUnregisterWorkQueueWithMMCSS function","base.rtwqbeginunregisterworkqueuewithmmcss","rtworkq/RtwqBeginUnregisterWorkQueueWithMMCSS"]
old-location: base\rtwqbeginunregisterworkqueuewithmmcss.htm
tech.root: backup
ms.assetid: 1faa9661-9b65-472a-b1d5-c99b10b149e9
ms.date: 12/05/2018
ms.keywords: RtwqBeginUnregisterWorkQueueWithMMCSS, RtwqBeginUnregisterWorkQueueWithMMCSS function, base.rtwqbeginunregisterworkqueuewithmmcss, rtworkq/RtwqBeginUnregisterWorkQueueWithMMCSS
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
 - RtwqBeginUnregisterWorkQueueWithMMCSS
 - rtworkq/RtwqBeginUnregisterWorkQueueWithMMCSS
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
 - RtwqBeginUnregisterWorkQueueWithMMCSS
---

# RtwqBeginUnregisterWorkQueueWithMMCSS function


## -description

Unregisters a work queue from a Multimedia Class Scheduler Service (MMCSS) task.

## -parameters

### -param workQueueId [in]

The identifier of the work queue.  For private work queues, the identifier is returned by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a> function.

### -param doneCallback [in]

Pointer to the <a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasynccallback">IRtwqAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param doneState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
