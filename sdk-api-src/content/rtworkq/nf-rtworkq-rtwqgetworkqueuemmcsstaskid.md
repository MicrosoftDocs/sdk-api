---
UID: NF:rtworkq.RtwqGetWorkQueueMMCSSTaskId
title: RtwqGetWorkQueueMMCSSTaskId function (rtworkq.h)
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier currently associated with this work queue. (RtwqGetWorkQueueMMCSSTaskId)
helpviewer_keywords: ["RtwqGetWorkQueueMMCSSTaskId","RtwqGetWorkQueueMMCSSTaskId function","base.rtwqgetworkqueuemmcsstaskid","rtworkq/RtwqGetWorkQueueMMCSSTaskId"]
old-location: base\rtwqgetworkqueuemmcsstaskid.htm
tech.root: backup
ms.assetid: b83314a4-1630-4e58-ba5b-e541002f23a3
ms.date: 12/05/2018
ms.keywords: RtwqGetWorkQueueMMCSSTaskId, RtwqGetWorkQueueMMCSSTaskId function, base.rtwqgetworkqueuemmcsstaskid, rtworkq/RtwqGetWorkQueueMMCSSTaskId
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
 - RtwqGetWorkQueueMMCSSTaskId
 - rtworkq/RtwqGetWorkQueueMMCSSTaskId
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
 - RtwqGetWorkQueueMMCSSTaskId
---

# RtwqGetWorkQueueMMCSSTaskId function


## -description

Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier currently associated with this work queue.

## -parameters

### -param workQueueId [in]

Identifier for the work queue. The identifier is retrieved by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a> function.

### -param taskId [out]

Receives the task identifier.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To associate a work queue with an MMCSS task, call <a href="/windows/win32/api/rtworkq/nf-rtworkq-rtwqbeginregisterworkqueuewithmmcss">RtwqBeginRegisterWorkQueueWithMMCSSEx</a>.
