---
UID: NF:ioringapi.SetIoRingCompletionEvent
tech.root: fs
title: SetIoRingCompletionEvent
ms.date: 04/21/2022
targetos: Windows
description: Registers a completion queue event with an IORING.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: ioringapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000 
req.target-min-winversvr: Windows Build 22000 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-core-ioring-l1-1-2.dll
 - api-ms-win-core-ioring-l1-1-1.dll
 - api-ms-win-core-ioring-l1-1-0.dll
 - ioringapi.h
api_name:
 - SetIoRingCompletionEvent
f1_keywords:
 - SetIoRingCompletionEvent
 - ioringapi/SetIoRingCompletionEvent
dev_langs:
 - c++
helpviewer_keywords:
 - SetIoRingCompletionEvent
---

## -description

Registers a completion queue event with an I/O ring.

## -parameters

### -param ioRing

An **HIORING** representing a handle to the I/O ring for which the completion event is registered.

### -param hEvent

A handle to the event object. The [CreateEvent](../synchapi/nf-synchapi-createeventa.md) or [OpenEvent](../synchapi/nf-synchapi-openeventa.md) function returns this handle.

## -returns

Returns an HRESULT including the following values:

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| E_INVALID_HANDLE | An invalid handle was passed in the *ioRing* parameter. |
| E_INVALIDARG | An invalid handle was passed in the *hEvent* parameter. |

## -remarks

The kernel will signal this event when it places the first entry into an empty completion queue, i.e. the kernel only sets the event to the signaled state when the completion queue transitions from the empty to non-empty state. Applications should call [PopIoRingCompletion](nf-ioringapi-popioringcompletion.md) until it indicates no more entries and then wait for any additional async completions to complete via the provided HANDLE. Otherwise, the event won’t enter the signaled state and the wait may block until a timeout occurs, or forever if an infinite timeout is used.

The kernel will internally duplicate the handle, so it is safe for the application to close the handle when waits are no longer needed. Providing an event handle value of NULL simply clears any existing value. Setting a value of INVALID_HANDLE_VALUE raises an error, as will any other invalid handle value, to aid in detecting code bugs early.

There is, at most, one event handle associated with an HIORING, attempting to set a second one will replace any that already exists.

## -see-also

[PopIoRingCompletion](nf-ioringapi-popioringcompletion.md)

