---
UID: NF:rtworkq.RtwqPutWaitingWorkItem
title: RtwqPutWaitingWorkItem function (rtworkq.h)
description: Queues a work item that waits for an event to be signaled. (RtwqPutWaitingWorkItem)
helpviewer_keywords: ["RtwqPutWaitingWorkItem","RtwqPutWaitingWorkItem function","base.rtwqputwaitingworkitem","rtworkq/RtwqPutWaitingWorkItem"]
old-location: base\rtwqputwaitingworkitem.htm
tech.root: backup
ms.assetid: 7cc7dd44-0949-49f7-8a8f-cc309650b763
ms.date: 12/05/2018
ms.keywords: RtwqPutWaitingWorkItem, RtwqPutWaitingWorkItem function, base.rtwqputwaitingworkitem, rtworkq/RtwqPutWaitingWorkItem
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
 - RtwqPutWaitingWorkItem
 - rtworkq/RtwqPutWaitingWorkItem
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
 - RtwqPutWaitingWorkItem
---

# RtwqPutWaitingWorkItem function


## -description

Queues a work item that waits for an event to be signaled.

## -parameters

### -param hEvent [in]

A handle to an event object, such as an event or timer. To create an event object, call <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> or <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventexa">CreateEventEx</a>.

### -param lPriority [in]

The priority of the work item. Work items are performed in order of priority.

### -param result [in]

A pointer to the <a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasyncresult">IRtwqAsyncResult</a> interface of an asynchronous result object. To create the result object, call <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqcreateasyncresult">RtwqCreateAsyncResult</a>.

### -param key [out, optional]

Receives a key that can be used to cancel the wait. To cancel the wait, call <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqcancelworkitem">RtwqCancelWorkItem</a> and pass this key in the <i>Key</i> parameter. This parameter can be <b>NULL</b>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
