---
UID: NF:winbase.HasOverlappedIoCompleted
title: HasOverlappedIoCompleted macro (winbase.h)
description: Provides a high performance test operation that can be used to poll for the completion of an outstanding I/O operation.
helpviewer_keywords: ["HasOverlappedIoCompleted","HasOverlappedIoCompleted macro","_win32_hasoverlappediocompleted","base.hasoverlappediocompleted","winbase/HasOverlappedIoCompleted"]
old-location: base\hasoverlappediocompleted.htm
tech.root: backup
ms.assetid: 1e2a3bf0-a73e-4406-99ac-32652f7f5b25
ms.date: 12/05/2018
ms.keywords: HasOverlappedIoCompleted, HasOverlappedIoCompleted macro, _win32_hasoverlappediocompleted, base.hasoverlappediocompleted, winbase/HasOverlappedIoCompleted
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - HasOverlappedIoCompleted
 - winbase/HasOverlappedIoCompleted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - HasOverlappedIoCompleted
---

# HasOverlappedIoCompleted macro


## -description

Provides a high performance test operation that can be used to poll for the completion of an outstanding I/O operation.

## -parameters

### -param lpOverlapped

A pointer to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that was specified when the overlapped I/O operation was started.

## -remarks

Do not call this macro unless the call to 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_IO_PENDING</b>, indicating that the overlapped I/O has started.

To cancel all pending asynchronous I/O operations, use the 
<a href="/windows/desktop/FileIO/cancelio">CancelIo</a> function. The <b>CancelIo</b> function only cancels operations issued by the calling thread for the specified file handle. I/O operations that are canceled complete with the error <b>ERROR_OPERATION_ABORTED</b>.

To get more details about a completed I/O operation, call the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.

## -see-also

<a href="/windows/desktop/FileIO/cancelio">CancelIo</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe">TransactNamedPipe</a>



<a href="/windows/desktop/api/winbase/nf-winbase-waitcommevent">WaitCommEvent</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>