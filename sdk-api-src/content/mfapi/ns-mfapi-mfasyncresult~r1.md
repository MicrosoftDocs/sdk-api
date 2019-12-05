---
UID: NS:mfapi.tagMFASYNCRESULT~r1
title: MFASYNCRESULT
ms.date: 01/30/19
ms.keywords: tagMFASYNCRESULT, MFASYNCRESULT
ms.topic: language-reference
f1_keywords:
- mfapi/tagMFASYNCRESULT
dev_langs:
- c++
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: mfapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: MFASYNCRESULT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
- apiref
api_type:
- HeaderDef
api_location:
- mfapi.h
api_name:
- tagMFASYNCRESULT
- MFASYNCRESULT
---

# MFASYNCRESULT structure


## -description

Contains data that is needed to implement the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface.


## -struct-fields

### -field AsyncResult

### -field overlapped

An <b>OVERLAPPED</b> structure. 
This structure is used internally to queue the work item. 
Fill this member with zeros.


### -field pCallback

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface. 
This interface is implemented by the caller of the asynchronous method. 
This member can be <b>NULL</b>. If this member is <b>NULL</b>, the <b>hEvent</b> member must be a valid event handle.


### -field hrStatusResult

The status code returned when this structure is used with an I/O completion port. 
You can also use this member to hold the status code for the asynchronous operation, returned by <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus">IMFAsyncResult::GetStatus</a>.


### -field dwBytesTransferred

The number of bytes transferred when this structure is used with an I/O completion port. 
This member is used internally by the work queue. Set this member to zero.


### -field hEvent

Event handle. If <b>pCallback</b> is <b>NULL</b>, set this member to a valid event handle. 
The event is signaled when the work item is dispatched. Otherwise, set this member to <b>NULL</b>.


## -remarks

Any custom implementation of the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface must inherit this structure. 
For more information, see <a href="https://docs.microsoft.com/windows/desktop/medfound/custom-asynchronous-result-objects">Custom Asynchronous Result Objects</a>.


## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/custom-asynchronous-result-objects">Custom Asynchronous Result Objects</a>

<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>

<a href="https://docs.microsoft.com/windows/desktop/medfound/work-queues">Work Queues</a>
 

 


