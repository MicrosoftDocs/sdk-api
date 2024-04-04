---
UID: NF:ioapiset.GetOverlappedResult
title: GetOverlappedResult function (ioapiset.h)
description: Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device.
helpviewer_keywords: ["GetOverlappedResult","GetOverlappedResult function","_win32_getoverlappedresult","base.getoverlappedresult","ioapiset/GetOverlappedResult","winbase/GetOverlappedResult"]
old-location: base\getoverlappedresult.htm
tech.root: backup
ms.assetid: 7f999959-9b22-4491-ae2b-a2674d821110
ms.date: 12/05/2018
ms.keywords: GetOverlappedResult, GetOverlappedResult function, _win32_getoverlappedresult, base.getoverlappedresult, ioapiset/GetOverlappedResult, winbase/GetOverlappedResult
req.header: ioapiset.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetOverlappedResult
 - ioapiset/GetOverlappedResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-io-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-io-l1-1-1.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
api_name:
 - GetOverlappedResult
---

# GetOverlappedResult function


## -description

Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device. To specify a timeout interval or wait on an alertable thread, use <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresultex">GetOverlappedResultEx</a>.

## -parameters

### -param hFile [in]

A handle to the file, named pipe, or communications device. This is the same handle that was specified when the overlapped operation was started by a call to any of the following functions: 

- [ReadFile](../fileapi/nf-fileapi-readfile.md)
- [WriteFile](../fileapi/nf-fileapi-writefile.md)
- [ConnectNamedPipe](../namedpipeapi/nf-namedpipeapi-connectnamedpipe.md)
- [TransactNamedPipe](../namedpipeapi/nf-namedpipeapi-transactnamedpipe.md)
- [DeviceIoControl](./nf-ioapiset-deviceiocontrol.md)
- [WaitCommEvent](../winbase/nf-winbase-waitcommevent.md)
- [ReadDirectoryChangesW](../winbase/nf-winbase-readdirectorychangesw.md)
- [LockFileEx](../fileapi/nf-fileapi-lockfileex.md)

### -param lpOverlapped [in]

A pointer to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that was specified when the overlapped operation was started.

### -param lpNumberOfBytesTransferred [out]

A pointer to a variable that receives the number of bytes that were actually transferred by a read or write operation. For a 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe">TransactNamedPipe</a> operation, this is the number of bytes that were read from the pipe. For a 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> operation, this is the number of bytes of output data returned by the device driver. For a 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-waitcommevent">WaitCommEvent</a> operation, this value is undefined.

### -param bWait [in]

If this parameter is <b>TRUE</b>, and the <b>Internal</b> member of the <i>lpOverlapped</i> structure is <b>STATUS_PENDING</b>, the function does not return until the operation has been completed. If this parameter is <b>FALSE</b> and the operation is still pending, the function returns <b>FALSE</b> and the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_IO_INCOMPLETE</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The results reported by the 
<b>GetOverlappedResult</b> function are those of the specified handle's last overlapped operation to which the specified 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure was provided, and for which the operation's results were pending. A pending operation is indicated when the function that started the operation returns <b>FALSE</b>, and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_IO_PENDING</b>. When an I/O operation is pending, the function that started the operation resets the <b>hEvent</b> member of the 
<b>OVERLAPPED</b> structure to the nonsignaled state. Then when the pending operation has been completed, the system sets the event object to the signaled state.

If the <i>bWait</i> parameter is <b>TRUE</b>, 
<b>GetOverlappedResult</b> determines whether the pending operation has been completed by waiting for the event object to be in the signaled state.

If the <b>hEvent</b> member of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure is <b>NULL</b>, the system uses the state of the <i>hFile</i> handle to signal when the operation has been completed. Use of file, named pipe, or communications-device handles for this purpose is discouraged. It is safer to use an event object because of the confusion that can occur when multiple simultaneous overlapped operations are performed on the same file, named pipe, or communications device. In this situation, there is no way to know which operation caused the object's state to be signaled.


#### Examples

For an example that uses **GetOverlappedResult**, see [Testing for the End of a File](/windows/win32/fileio/testing-for-the-end-of-a-file)

## -see-also

[CancelIo](/windows/win32/FileIO/cancelio), [CreateEvent](../synchapi/nf-synchapi-createeventa.md), [GetOverlappedResultEx](./nf-ioapiset-getoverlappedresultex.md), [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md), [Overlapped Input and Output](/windows/win32/Sync/synchronization-and-overlapped-input-and-output), [Synchronization Functions](/windows/win32/Sync/synchronization-functions)
