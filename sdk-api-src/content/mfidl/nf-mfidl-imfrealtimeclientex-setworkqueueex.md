---
UID: NF:mfidl.IMFRealTimeClientEx.SetWorkQueueEx
title: IMFRealTimeClientEx::SetWorkQueueEx (mfidl.h)
description: Specifies the work queue that this object should use for asynchronous work items.
helpviewer_keywords: ["IMFRealTimeClientEx interface [Media Foundation]","SetWorkQueueEx method","IMFRealTimeClientEx.SetWorkQueueEx","IMFRealTimeClientEx::SetWorkQueueEx","SetWorkQueueEx","SetWorkQueueEx method [Media Foundation]","SetWorkQueueEx method [Media Foundation]","IMFRealTimeClientEx interface","mf.imfrealtimeclientex_setworkqueueex","mfidl/IMFRealTimeClientEx::SetWorkQueueEx"]
old-location: mf\imfrealtimeclientex_setworkqueueex.htm
tech.root: mf
ms.assetid: 4F91FD8A-A8B6-4066-A0EB-F764A3BFD8A2
ms.date: 12/05/2018
ms.keywords: IMFRealTimeClientEx interface [Media Foundation],SetWorkQueueEx method, IMFRealTimeClientEx.SetWorkQueueEx, IMFRealTimeClientEx::SetWorkQueueEx, SetWorkQueueEx, SetWorkQueueEx method [Media Foundation], SetWorkQueueEx method [Media Foundation],IMFRealTimeClientEx interface, mf.imfrealtimeclientex_setworkqueueex, mfidl/IMFRealTimeClientEx::SetWorkQueueEx
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFRealTimeClientEx::SetWorkQueueEx
 - mfidl/IMFRealTimeClientEx::SetWorkQueueEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFRealTimeClientEx.SetWorkQueueEx
---

# IMFRealTimeClientEx::SetWorkQueueEx


## -description

Specifies the work queue that this object should use for asynchronous work items.

## -parameters

### -param dwMultithreadedWorkQueueId

The work queue identifier.

### -param lWorkItemBasePriority

The base priority for work items.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The object should use the values of <i>dwMultithreadedWorkQueueId</i> and <i>lWorkItemBasePriority</i> when it queues new work items. Use the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem2">MFPutWorkItem2</a> or <a href="/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex2">MFPutWorkItemEx2</a> function to queue the work item.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex">IMFRealTimeClientEx</a>



<a href="/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>