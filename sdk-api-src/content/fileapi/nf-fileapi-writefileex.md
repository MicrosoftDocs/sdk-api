---
UID: NF:fileapi.WriteFileEx
title: WriteFileEx function (fileapi.h)
description: Writes data to the specified file or input/output (I/O) device. It reports its completion status asynchronously, calling the specified completion routine when writing is completed or canceled and the calling thread is in an alertable wait state.
helpviewer_keywords: ["WriteFileEx","WriteFileEx function [Files]","_win32_writefileex","base.writefileex","fileapi/WriteFileEx","fs.writefileex","winbase/WriteFileEx"]
old-location: fs\writefileex.htm
tech.root: fs
ms.assetid: 6995c4ee-ba91-41d5-b72d-19dc2eb95945
ms.date: 02/13/2023
ms.keywords: WriteFileEx, WriteFileEx function [Files], _win32_writefileex, base.writefileex, fileapi/WriteFileEx, fs.writefileex, winbase/WriteFileEx
req.header: fileapi.h
req.include-header: Windows.h
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
 - WriteFileEx
 - fileapi/WriteFileEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - WriteFileEx
---

# WriteFileEx function

## -description

Writes data to the specified file or input/output (I/O) device. It reports its completion status asynchronously, calling the specified completion routine when writing is completed or canceled and the calling thread is in an alertable wait state.

To write data to a file or device synchronously, use the [WriteFile](/windows/win32/api/fileapi/nf-fileapi-writefile) function.

## -parameters

### -param hFile [in]

A handle to the file or I/O device (for example, a file, file stream, physical disk, volume,  console buffer, tape drive, socket, communications resource, mailslot, or  pipe).

This parameter can be any handle opened with the **FILE_FLAG_OVERLAPPED** flag by the [CreateFile](/windows/win32/api/fileapi/nf-fileapi-createfilea) function, or a socket handle returned by the [socket](/windows/win32/api/winsock2/nf-winsock2-socket) or [accept](/windows/win32/api/winsock2/nf-winsock2-accept) function.

Do not associate an I/O completion port with this handle. For more information, see the Remarks section.

This handle also must have the **GENERIC_WRITE** access right. For more information on access rights, see [File Security and Access Rights](/windows/win32/FileIO/file-security-and-access-rights).

### -param lpBuffer [in, optional]

A pointer to the buffer containing the data to be written to the file or device.

This buffer must remain valid for the duration of the write operation. The caller must not use this buffer until the write operation is completed.

### -param nNumberOfBytesToWrite [in]

The number of bytes to be written to the file or device.

A value of zero specifies a null write operation. The behavior of a null write operation depends on the underlying file system.

Pipe write operations across a network are limited to 65,535 bytes per write. For more information regarding  pipes, see the Remarks section.

### -param lpOverlapped [in, out]

A pointer to an [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) data structure that supplies data to be used during the overlapped (asynchronous) write operation.

For files that support byte offsets, you must specify a byte offset at which to start writing to the file. You specify this offset by setting the **Offset** and **OffsetHigh** members of the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure. For files or devices that do not support byte offsets, **Offset** and **OffsetHigh** are ignored.

To write to the end of file, specify both the **Offset** and **OffsetHigh** members of the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure as `0xFFFFFFFF`. This is functionally equivalent to previously calling the [CreateFile](/windows/win32/api/fileapi/nf-fileapi-createfilea) function to open _hFile_ using **FILE_APPEND_DATA** access.

The **WriteFileEx** function ignores the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure's **hEvent** member. An application is free to use that member for its own purposes in the context of a **WriteFileEx** call. **WriteFileEx** signals completion of its writing operation by calling, or queuing a call to, the completion routine pointed to by _lpCompletionRoutine_, so it does not need an event handle.

The **WriteFileEx** function does use the **Internal** and **InternalHigh** members of the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure. You should not change the value of these members.

The [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) data structure must remain valid for the duration of the write operation. It should not be a variable that can go out of scope while the write operation is pending completion.

### -param lpCompletionRoutine [in]

A pointer to a completion routine to be called when the write operation has been completed and the calling thread is in an alertable wait state. For more information about this completion routine, see [FileIOCompletionRoutine](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine).

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

If the **WriteFileEx** function succeeds, the calling thread has an asynchronous I/O operation pending: the overlapped write operation to the file. When this I/O operation finishes, and the calling thread is blocked in an alertable wait state, the operating system calls the function pointed to by _lpCompletionRoutine_, and the wait completes with a return code of `WAIT_IO_COMPLETION`.

If the function succeeds and the file-writing operation finishes, but the calling thread is not in an alertable wait state, the system queues the call to *_lpCompletionRoutine_, holding the call until the calling thread enters an alertable wait state. For more information about alertable wait states and overlapped input/output operations, see [About Synchronization](/windows/win32/Sync/about-synchronization).

## -remarks

When using **WriteFileEx** you should check [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) even when the function returns "success" to check for conditions that are _successes_ but have some outcome you might want to know about. For example, a buffer overflow when calling **WriteFileEx** will return `TRUE`, but **GetLastError** will report the overflow with `ERROR_MORE_DATA`. If the function call is successful and there are no warning conditions, **GetLastError** will return `ERROR_SUCCESS`.

The **WriteFileEx** function will fail if the _hFile_ parameter is associated with an [I/O completion port](/windows/win32/FileIO/i-o-completion-ports). To perform writes using this type of handle, use the [WriteFile](/windows/win32/api/fileapi/nf-fileapi-writefile) function.

The **WriteFileEx** function may fail if there are too many outstanding asynchronous I/O requests. In the event of such a failure, [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) can return `ERROR_INVALID_USER_BUFFER` or `ERROR_NOT_ENOUGH_MEMORY`.

To cancel all pending asynchronous I/O operations, use either:

- [CancelIo](/windows/win32/FileIO/cancelio): This function only cancels operations issued by the calling thread for the specified file handle.
- [CancelIoEx](/windows/win32/FileIO/cancelioex-func): This function cancels all operations issued by the threads for the specified file handle.

Use [CancelSynchronousIo](/windows/win32/FileIO/cancelsynchronousio-func) to cancel pending synchronous I/O operations.

I/O operations that are canceled complete with the error **ERROR_OPERATION_ABORTED**.

If part of the file specified by _hFile_ is locked by another process, and the specified write operation overlaps the locked portion, **WriteFileEx** fails.

When writing to a file, the last write time is not fully updated until all handles used for writing have been closed. Therefore, to ensure an accurate last write time, close the file handle immediately after writing to the file.

Accessing the output buffer while a write operation is using the buffer may lead to corruption of the data written from that buffer. Applications must not write to, reallocate, or free the output buffer that a write operation is using until the write operation completes.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use unbuffered I/O.

The system interprets zero bytes to write as specifying a null write operation and [WriteFile](/windows/win32/api/fileapi/nf-fileapi-writefile) does not truncate or extend the file. To truncate or extend a file, use the [SetEndOfFile](/windows/win32/api/fileapi/nf-fileapi-setendoffile) function.

An application uses the [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [WaitForMultipleObjectsEx](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex), [MsgWaitForMultipleObjectsEx](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex), [SignalObjectAndWait](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), and [SleepEx](/windows/win32/api/synchapi/nf-synchapi-sleepex) functions to enter an alertable wait state. For more information about alertable wait states and overlapped I/O operations, see [About Synchronization](/windows/win32/Sync/about-synchronization).

If you write directly to a volume that has a mounted file system, you must first obtain exclusive access to the volume. Otherwise, you risk causing data corruption or system instability, because your application's writes may conflict with other changes coming from the file system and leave the contents of the volume in an inconsistent state. To prevent these problems, the following changes have been made in Windows Vista and later:

- A write on a volume handle will succeed if the volume does not have a mounted file system, or if one of the following conditions is true:
  - The sectors to be written to are boot sectors.
  - The sectors to be written to reside outside of file system space.
  - You have explicitly locked or dismounted the volume by using [FSCTL_LOCK_VOLUME](/windows/win32/api/winioctl/ni-winioctl-fsctl_lock_volume) or [FSCTL_DISMOUNT_VOLUME](/windows/win32/api/winioctl/ni-winioctl-fsctl_dismount_volume).
  - The volume has no actual file system. (In other words, it has a RAW file system mounted.)
- A write on a disk handle will succeed if one of the following conditions is true:
  - The sectors to be written to do not fall within a volume's extents.
  - The sectors to be written to fall within a mounted volume, but you have explicitly locked or dismounted the volume by using [FSCTL_LOCK_VOLUME](/windows/win32/api/winioctl/ni-winioctl-fsctl_lock_volume) or [FSCTL_DISMOUNT_VOLUME](/windows/win32/api/winioctl/ni-winioctl-fsctl_dismount_volume).
  - The sectors to be written to fall within a volume that has no mounted file system other than RAW.

There are strict requirements for successfully working with files opened with [CreateFile](/windows/win32/api/fileapi/nf-fileapi-createfilea) using **FILE_FLAG_NO_BUFFERING**. For details see [File Buffering](/windows/win32/FileIO/file-buffering).

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

| Technology | Supported |
|--------|--------|
| Server Message Block (SMB) 3.0 protocol | Yes |
| SMB 3.0 Transparent Failover (TFO) | Yes |
| SMB 3.0 with Scale-out File Shares (SO) | Yes |
| Cluster Shared Volume File System (CsvFS) | Yes |
| Resilient File System (ReFS) | Yes |

### Transacted Operations

If there is a transaction bound to the file handle, then the file write is transacted. For more information, see [About Transactional NTFS](/windows/win32/FileIO/about-transactional-ntfs).

### Examples

For an example, see [Named Pipe Server Using Completion Routines](/windows/win32/ipc/named-pipe-server-using-completion-routines).

## -see-also

- [CancelIo](/windows/win32/FileIO/cancelio)

- [CancelIoEx](/windows/win32/FileIO/cancelioex-func)

- [CancelSynchronousIo](/windows/win32/FileIO/cancelsynchronousio-func)

- [CreateFile](/windows/win32/api/fileapi/nf-fileapi-createfilea)

- [File Management Functions](/windows/win32/FileIO/file-management-functions)

- [FileIOCompletionRoutine](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine)

- [MsgWaitForMultipleObjectsEx](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

- [ReadFileEx](/windows/win32/api/fileapi/nf-fileapi-readfileex)

- [SetEndOfFile](/windows/win32/api/fileapi/nf-fileapi-setendoffile)

- [SetErrorMode](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode)

- [SignalObjectAndWait](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)

- [SleepEx](/windows/win32/api/synchapi/nf-synchapi-sleepex)

- [WaitForMultipleObjectsEx](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)

- [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)

- [WriteFile](/windows/win32/api/fileapi/nf-fileapi-writefile)
