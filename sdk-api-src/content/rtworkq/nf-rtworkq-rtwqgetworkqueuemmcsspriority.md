---
UID: NF:rtworkq.RtwqGetWorkQueueMMCSSPriority
title: RtwqGetWorkQueueMMCSSPriority function (rtworkq.h)
description: Gets the relative thread priority of a work queue. (RtwqGetWorkQueueMMCSSPriority)
helpviewer_keywords: ["RtwqGetWorkQueueMMCSSPriority","RtwqGetWorkQueueMMCSSPriority function","base.rtwqgetworkqueuemmcsspriority","rtworkq/RtwqGetWorkQueueMMCSSPriority"]
old-location: base\rtwqgetworkqueuemmcsspriority.htm
tech.root: backup
ms.assetid: c9f18299-bd0a-4c1c-acc0-2cc8bc84aa82
ms.date: 12/05/2018
ms.keywords: RtwqGetWorkQueueMMCSSPriority, RtwqGetWorkQueueMMCSSPriority function, base.rtwqgetworkqueuemmcsspriority, rtworkq/RtwqGetWorkQueueMMCSSPriority
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
 - RtwqGetWorkQueueMMCSSPriority
 - rtworkq/RtwqGetWorkQueueMMCSSPriority
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
 - RtwqGetWorkQueueMMCSSPriority
---

# RtwqGetWorkQueueMMCSSPriority function


## -description

Gets the relative thread priority of a work queue.

## -parameters

### -param workQueueId [in]

The identifier of the work queue. For private work queues, the identifier is returned by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a> function.

### -param priority [out]

Receives the relative thread priority.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function returns the relative thread priority set by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqbeginregisterworkqueuewithmmcss">RtwqBeginRegisterWorkQueueWithMMCSS</a> function.
