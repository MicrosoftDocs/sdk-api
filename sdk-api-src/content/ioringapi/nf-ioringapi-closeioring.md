---
UID: NF:ioringapi.CloseIoRing
tech.root: fs
title: CloseIoRing
ms.date: 07/16/2021
targetos: Windows
description: Closes an **HIORING** handle that was previously opened with a call to CreateIoRing.
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
 - CloseIoRing
f1_keywords:
 - CloseIoRing
 - ioringapi/CloseIoRing
dev_langs:
 - c++
---

## -description

Closes an **HIORING** handle that was previously opened with a call to [CreateIoRing](nf-ioringapi-createioring.md).

## -parameters

### -param ioRing

The **HIORING** handle to close.

## -returns

Returns S_OK on success.

## -remarks

Calling this function ensures that resources allocated for the I/O ring are released. The closed handle is no longer valid after the function returns. It is important to note that closing the handle abandons the operations that are queued but not submitted.  However, the operations that are in flight are **not** cancelled. 

It is possible that reads from or writes to memory buffers may still occur after **CloseIoRing** returns. If you want to ensure that no pending reads or writes occur, you must wait for the completions to appear in the completion queue for all the operations that are submitted. You may choose to cancel the previously submitted operations before waiting on their completions. As an alternative to submitting multiple cancel requests, you can call [CancelIoEx](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) with the file handle and NULL for the overlapped pointer to effectively cancel all pending operations on the handle.

## -see-also

