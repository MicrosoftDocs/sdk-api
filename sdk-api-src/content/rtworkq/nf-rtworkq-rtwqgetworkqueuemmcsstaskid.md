---
UID: NF:rtworkq.RtwqGetWorkQueueMMCSSTaskId
title: RtwqGetWorkQueueMMCSSTaskId function (rtworkq.h)
author: windows-sdk-content
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier currently associated with this work queue.
old-location: base\rtwqgetworkqueuemmcsstaskid.htm
tech.root: ProcThread
ms.assetid: b83314a4-1630-4e58-ba5b-e541002f23a3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RtwqGetWorkQueueMMCSSTaskId, RtwqGetWorkQueueMMCSSTaskId function, base.rtwqgetworkqueuemmcsstaskid, rtworkq/RtwqGetWorkQueueMMCSSTaskId
ms.topic: function
f1_keywords: 
 - "rtworkq/RtwqGetWorkQueueMMCSSTaskId"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqGetWorkQueueMMCSSTaskId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RtwqGetWorkQueueMMCSSTaskId function


## -description



Retrieves the Multimedia Class Scheduler Service (MMCSS) task identifier currently associated with this work queue.




## -parameters




### -param workQueueId [in]

Identifier for the work queue. The identifier is retrieved by the <a href="https://docs.microsoft.com/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a> function.


### -param taskId [out]

Receives the task identifier.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks

To associate a work queue with an MMCSS task, call <a href="<a href="/windows/win32/api/rtworkq/nf-rtworkq-rtwqbeginregisterworkqueuewithmmcss">RtwqBeginRegisterWorkQueueWithMMCSSEx</a>">RtwqBeginRegisterWorkQueueWithMMCSSEx</a>.
