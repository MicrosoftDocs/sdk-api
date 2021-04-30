---
UID: NS:mfapi.tagMFASYNCRESULT
title: MFASYNCRESULT (mfapi.h)
description: Contains data that is needed to implement the IMFAsyncResult interface.
helpviewer_keywords: ["MFASYNCRESULT","MFASYNCRESULT structure [Media Foundation]","fffa32d6-5e9f-42a1-9978-04f5726528bc","mf.mfasyncresult","mfapi/MFASYNCRESULT"]
old-location: mf\mfasyncresult.htm
tech.root: mf
ms.assetid: fffa32d6-5e9f-42a1-9978-04f5726528bc
ms.date: 12/05/2018
ms.keywords: MFASYNCRESULT, MFASYNCRESULT structure [Media Foundation], fffa32d6-5e9f-42a1-9978-04f5726528bc, mf.mfasyncresult, mfapi/MFASYNCRESULT
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFASYNCRESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMFASYNCRESULT
 - mfapi/tagMFASYNCRESULT
 - MFASYNCRESULT
 - mfapi/MFASYNCRESULT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFASYNCRESULT
---

# MFASYNCRESULT structure overview


## -description

Contains data that is needed to implement the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface.

## -struct-fields

### -field overlapped

An <b>OVERLAPPED</b> structure. This structure is used internally to queue the work item. Fill this member with zeros.

### -field pCallback

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface. This interface is implemented by the caller of the asynchronous method. This member can be <b>NULL</b>. If this member is <b>NULL</b>, the <b>hEvent</b> member must be a valid event handle.

### -field hrStatusResult

The status code returned when this structure is used with an I/O completion port. You can also use this member to hold the status code for the asynchronous operation, returned by <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus">IMFAsyncResult::GetStatus</a>.

### -field dwBytesTransferred

The number of bytes transferred when this structure is used with an I/O completion port. This member is used internally by the work queue. Set this member to zero.

### -field hEvent

Event handle. If <b>pCallback</b> is <b>NULL</b>, set this member to a valid event handle. The event is signaled when the work item is dispatched. Otherwise, set this member to <b>NULL</b>.

### -field IMFAsyncResult

## -remarks

Any custom implementation of the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface must inherit this structure. For more information, see <a href="/windows/desktop/medfound/custom-asynchronous-result-objects">Custom Asynchronous Result Objects</a>.

## -see-also

<a href="/windows/desktop/medfound/custom-asynchronous-result-objects">Custom Asynchronous Result Objects</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>