---
UID: NE:combaseapi.tagCOWAIT_FLAGS
title: COWAIT_FLAGS (combaseapi.h)
description: Specifies the behavior of the CoWaitForMultipleHandles function.
helpviewer_keywords: ["COWAIT_ALERTABLE","COWAIT_DEFAULT","COWAIT_DISPATCH_CALLS","COWAIT_DISPATCH_WINDOW_MESSAGES","COWAIT_FLAGS","COWAIT_FLAGS enumeration [COM]","COWAIT_INPUTAVAILABLE","COWAIT_WAITALL","_com_COWAIT_FLAGS","com.cowait_flags","combaseapi/COWAIT_ALERTABLE","combaseapi/COWAIT_DEFAULT","combaseapi/COWAIT_DISPATCH_CALLS","combaseapi/COWAIT_DISPATCH_WINDOW_MESSAGES","combaseapi/COWAIT_FLAGS","combaseapi/COWAIT_INPUTAVAILABLE","combaseapi/COWAIT_WAITALL"]
old-location: com\cowait_flags.htm
tech.root: com
ms.assetid: e6f8300c-f74b-4383-8ee5-519a0ed0b358
ms.date: 12/05/2018
ms.keywords: COWAIT_ALERTABLE, COWAIT_DEFAULT, COWAIT_DISPATCH_CALLS, COWAIT_DISPATCH_WINDOW_MESSAGES, COWAIT_FLAGS, COWAIT_FLAGS enumeration [COM], COWAIT_INPUTAVAILABLE, COWAIT_WAITALL, _com_COWAIT_FLAGS, com.cowait_flags, combaseapi/COWAIT_ALERTABLE, combaseapi/COWAIT_DEFAULT, combaseapi/COWAIT_DISPATCH_CALLS, combaseapi/COWAIT_DISPATCH_WINDOW_MESSAGES, combaseapi/COWAIT_FLAGS, combaseapi/COWAIT_INPUTAVAILABLE, combaseapi/COWAIT_WAITALL
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: COWAIT_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOWAIT_FLAGS
 - combaseapi/tagCOWAIT_FLAGS
 - COWAIT_FLAGS
 - combaseapi/COWAIT_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - combaseapi.h
api_name:
 - COWAIT_FLAGS
---

# COWAIT_FLAGS enumeration


## -description

Specifies the behavior of the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a> function.

## -enum-fields

### -field COWAIT_DEFAULT:0

Dispatch calls needed for marshaling without dispatching arbitrary calls.

### -field COWAIT_WAITALL:1

If set, the call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a> will return S_OK only when all handles associated with the synchronization object have been signaled and an input event has been received, all at the same time.  In this case, the behavior of <b>CoWaitForMultipleHandles</b> corresponds to  the behavior of the <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a> function with the <i>dwFlags</i> parameter set to <b>MWMO_WAITALL</b>. If <b>COWAIT_WAITALL</b> is not set, the call to <b>CoWaitForMultipleHandles</b> will return S_OK as soon as any handle associated with the synchronization object has been signaled, regardless of whether an input event is received.

### -field COWAIT_ALERTABLE:2

If set, the call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a> will return S_OK if an asynchronous procedure call (APC) has been queued to the calling thread with a call to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a> function, even if no handle has been signaled.

### -field COWAIT_INPUTAVAILABLE:4

If set, the call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a> will return S_OK  if input exists for the queue, even if the input has been seen (but not removed) using a call to another function, such as <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea">PeekMessage</a>.

### -field COWAIT_DISPATCH_CALLS:8

Dispatch calls from <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a> in an ASTA. Default is no call dispatch. This value has no meaning in other apartment types and is ignored.

### -field COWAIT_DISPATCH_WINDOW_MESSAGES:0x10

Enables dispatch of window messages from <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a> in an ASTA or STA. Default in ASTA is no window messages dispatched, default in STA is only a small set of special-cased messages dispatched. The value has no meaning in MTA and is ignored.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles">CoWaitForMultipleHandles</a>



<a href="/windows/desktop/api/objidl/nf-objidl-isynchronize-wait">ISynchronize::Wait</a>



<a href="/windows/desktop/api/objidl/nf-objidl-isynchronizecontainer-waitmultiple">ISynchronizeContainer::WaitMultiple</a>
