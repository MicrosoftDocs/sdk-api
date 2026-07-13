---
UID: NF:fileapi.WriteFile
title: WriteFile function (fileapi.h)
description: Writes data to the specified file or input/output (I/O) device.
helpviewer_keywords: ["WriteFile","WriteFile function [Files]","_win32_writefile","base.writefile","fileapi/WriteFile","fs.writefile","winbase/WriteFile"]
old-location: fs\writefile.htm
tech.root: fs
ms.assetid: 9d6fa723-fe3e-4052-b0b3-2686eee076a7
ms.date: 02/28/2025
ms.keywords: WriteFile, WriteFile function [Files], _win32_writefile, base.writefile, fileapi/WriteFile, fs.writefile, winbase/WriteFile
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
 - WriteFile
 - fileapi/WriteFile
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
 - WriteFile
---

# WriteFile function

## -description

Writes data to the specified file or input/output (I/O) device.

This function is designed for both synchronous and asynchronous operation. For a similar function designed solely for asynchronous operation, see [WriteFileEx](nf-fileapi-writefileex.md).

## -parameters

### -param hFile [in]

A handle to the file or I/O device (for example, a file, file stream, physical disk, volume,  console buffer, tape drive, socket, communications resource, mailslot, or  pipe).

The *hFile* parameter must have been created with the write access. For more information, see [Generic Access Rights](/windows/win32/SecAuthZ/generic-access-rights) and [File Security and Access Rights](/windows/win32/FileIO/file-security-and-access-rights).

For asynchronous write operations, *hFile* can be any handle opened with the [CreateFile](nf-fileapi-createfilea.md) function using the **FILE_FLAG_OVERLAPPED** flag or a socket handle returned by the [socket](/windows/win32/api/winsock2/nf-winsock2-socket) or [accept](/windows/win32/api/winsock2/nf-winsock2-accept) function.

### -param lpBuffer [in]

A pointer to the buffer containing the data to be written to the file or device.

This buffer must remain valid for the duration of the write operation. The caller must not use this buffer until the write operation is completed.

### -param nNumberOfBytesToWrite [in]

The number of bytes to be written to the file or device.

A value of zero specifies a null write operation. The behavior of a null write operation depends on the underlying file system or communications technology.

**Windows Server 2003 and Windows XP:** Pipe write operations across a network are limited in size per write. The amount varies per platform. For x86 platforms it's 63.97 MB. For x64 platforms it's 31.97 MB. For Itanium it's 63.95 MB. For more information regarding pipes, see the Remarks section.

### -param lpNumberOfBytesWritten [out, optional]

A pointer to the variable that receives the number of bytes written when using a synchronous *hFile* parameter. **WriteFile** sets this value to zero before doing any work or error checking. Use `NULL` for this parameter if this is an asynchronous operation to avoid potentially erroneous results.

This parameter can be `NULL` only when the *lpOverlapped* parameter is not `NULL`.

**Windows 7:** This parameter can not be `NULL`.

For more information, see the Remarks section.

### -param lpOverlapped [in, out, optional]

A pointer to an [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure is required if the *hFile* parameter was opened with **FILE_FLAG_OVERLAPPED**, otherwise this parameter can be `NULL`.

For an *hFile* that supports byte offsets, if you use this parameter you must specify a byte offset at which to start writing to the file or device. This offset is specified by setting the **Offset** and **OffsetHigh** members of the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure. For an *hFile* that does not support byte offsets, **Offset** and **OffsetHigh** are ignored.

To write to the end of file, specify both the **Offset** and **OffsetHigh** members of the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure as `0xFFFFFFFF`. This is functionally equivalent to previously calling the [CreateFile](nf-fileapi-createfilea.md) function to open *hFile* using **FILE_APPEND_DATA** access.

For more information about different combinations of *lpOverlapped* and **FILE_FLAG_OVERLAPPED**, see the Remarks section and the [Synchronization and File Position](#synchronization-and-file-position) section.

## -returns

If the function succeeds, the return value is nonzero (**TRUE**).

If the function fails, or is completing asynchronously, the return value is zero (**FALSE**). To get extended error information, call the [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.

> [!NOTE]
> The [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) code **ERROR_IO_PENDING** is not a failure; it designates the write operation is pending completion asynchronously. For more information, see [Remarks](#-remarks).

## -remarks

The **WriteFile** function returns when one of the following conditions occur:

- The number of bytes requested is written.
- A read operation releases buffer space on the read end of the pipe (if the write was blocked). For more information, see the [Pipes](#pipes) section.
- An asynchronous handle is being used and the write is occurring asynchronously.
- An error occurs.

The **WriteFile** function may fail with **ERROR_INVALID_USER_BUFFER** or **ERROR_NOT_ENOUGH_MEMORY** whenever there are too many outstanding asynchronous I/O requests.

To cancel all pending asynchronous I/O operations, use either:

- [CancelIo](/windows/win32/FileIO/cancelio) — This function cancels only operations issued by the calling thread for the specified file handle.
- [CancelIoEx](/windows/win32/FileIO/cancelioex-func) - This function cancels all operations issued by the threads for the specified file handle.

Use the [CancelSynchronousIo](/windows/win32/FileIO/cancelsynchronousio-func) function to cancel pending synchronous I/O operations.

I/O operations that are canceled complete with the error **ERROR_OPERATION_ABORTED**.

The **WriteFile** function may fail with **ERROR_NOT_ENOUGH_QUOTA**, which means the calling process's buffer could not be page-locked. For more information, see [SetProcessWorkingSetSize](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsize).

If part of the file is locked by another process and the write operation overlaps the locked portion, **WriteFile** fails.

When writing to a file, the last write time is not fully updated until all handles used for writing have been closed. Therefore, to ensure an accurate last write time, close the file handle immediately after writing to the file.

Accessing the output buffer while a write operation is using the buffer may lead to corruption of the data written from that buffer. Applications must not write to, reallocate, or free the output buffer that a write operation is using until the write operation completes. This can be particularly problematic when using an asynchronous file handle. Additional information regarding synchronous versus asynchronous file handles can be found later in the [Synchronization and File Position](#synchronization-and-file-position) section and [Synchronous and Asynchronous I/O](/windows/win32/FileIO/synchronous-and-asynchronous-i-o).

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use unbuffered I/O.

The system interprets zero bytes to write as specifying a null write operation and **WriteFile** does not truncate or extend the file. To truncate or extend a file, use the [SetEndOfFile](nf-fileapi-setendoffile.md) function.

Characters can be written to the screen buffer using **WriteFile** with a handle to console output. The exact behavior of the function is determined by the console mode. The data is written to the current cursor position. The cursor position is updated after the write operation. For more information about console handles, see [CreateFile](nf-fileapi-createfilea.md).

When writing to a communications device, the behavior of **WriteFile** is determined by the current communication time-out as set and retrieved by using the [SetCommTimeouts](/windows/win32/api/winbase/nf-winbase-setcommtimeouts) and [GetCommTimeouts](/windows/win32/api/winbase/nf-winbase-getcommtimeouts) functions. Unpredictable results can occur if you fail to set the time-out values. For more information about communication time-outs, see [COMMTIMEOUTS](/windows/win32/api/winbase/ns-winbase-commtimeouts).

Although a single-sector write is atomic, a multi-sector write is not guaranteed to be atomic unless you are using a transaction (that is, the handle created is a transacted handle; for example, a handle created using [CreateFileTransacted](/windows/win32/api/winbase/nf-winbase-createfiletransacteda)). Multi-sector writes that are cached may not always be written to the disk right away; therefore, specify **FILE_FLAG_WRITE_THROUGH** in [CreateFile](nf-fileapi-createfilea.md) to ensure that an entire multi-sector write is written to the disk without potential caching delays.

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

There are strict requirements for successfully working with files opened with [CreateFile](nf-fileapi-createfilea.md) using **FILE_FLAG_NO_BUFFERING**. For details see [File Buffering](/windows/win32/FileIO/file-buffering).

If *hFile* was opened with **FILE_FLAG_OVERLAPPED**, the following conditions are in effect:

- The *lpOverlapped* parameter must point to a valid and unique [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure, otherwise the function can incorrectly report that the write operation is complete.
- The *lpNumberOfBytesWritten* parameter should be set to `NULL`. To get the number of bytes written, use the [GetOverlappedResult](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) function. If the *hFile* parameter is associated with an I/O completion port, you can also get the number of bytes written by calling the [GetQueuedCompletionStatus](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.

In Windows Server 2012, this function is supported by the following technologies.

| Technology | Supported |
| ---------- | --------- |
| Server Message Block (SMB) 3.0 protocol | Yes |
| SMB 3.0 Transparent Failover (TFO) | Yes |
| SMB 3.0 with Scale-out File Shares (SO) | Yes |
| Cluster Shared Volume File System (CsvFS) | Yes |
| Resilient File System (ReFS) | Yes |

#### Synchronization and File Position

If *hFile* is opened with **FILE_FLAG_OVERLAPPED**, it is an asynchronous file handle; otherwise it is synchronous. The rules for using the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure are slightly different for each, as previously noted.

> [!NOTE]
> If a file or device is opened for asynchronous I/O, subsequent calls to functions such as **WriteFile** using that handle generally return immediately, but can also behave synchronously with respect to blocked execution. For more information, see [Asynchronous disk I/O appears as synchronous on Windows](/previous-versions/troubleshoot/windows/win32/asynchronous-disk-io-synchronous).

Considerations for working with asynchronous file handles:

- **WriteFile** may return before the write operation is complete. In this scenario, **WriteFile** returns **FALSE** and the [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns **ERROR_IO_PENDING**, which allows the calling process to continue while the system completes the write operation.
- The *lpOverlapped* parameter must not be `NULL` and should be used with the following facts in mind:
  - Although the event specified in the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure is set and reset automatically by the system, the offset that is specified in the **OVERLAPPED** structure is not automatically updated.
  - **WriteFile** resets the event to a non-signaled state when it begins the I/O operation.
  - The event specified in the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure is set to a signaled state when the write operation is complete; until that time, the write operation is considered pending.
  - Because the write operation starts at the offset that is specified in the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure, and **WriteFile** may return before the system-level write operation is complete (write pending), neither the offset nor any other part of the structure should be modified, freed, or reused by the application until the event is signaled (that is, the write completes).

Considerations for working with synchronous file handles:

- If *lpOverlapped* is `NULL`, the write operation starts at the current file position and **WriteFile** does not return until the operation is complete, and the system updates the file pointer before **WriteFile** returns.
- If *lpOverlapped* is not `NULL`, the write operation starts at the offset that is specified in the [OVERLAPPED](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) structure and **WriteFile** does not return until the write operation is complete. The system updates the **OVERLAPPED** `Internal` and `InternalHigh` fields and the file pointer before **WriteFile** returns.

For more information, see [CreateFile](nf-fileapi-createfilea.md) and [Synchronous and Asynchronous I/O](/windows/win32/FileIO/synchronous-and-asynchronous-i-o).

#### Pipes

If an anonymous pipe is being used and the read handle has been closed, when **WriteFile** attempts to write using the pipe's corresponding write handle, the function returns **FALSE** and [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR_BROKEN_PIPE**.

If the pipe buffer is full when an application uses the **WriteFile** function to write to a pipe, the write operation may not finish immediately. The write operation will be completed when a read operation (using the [ReadFile](nf-fileapi-readfile.md) function) makes more system buffer space available for the pipe.

When writing to a non-blocking, byte-mode pipe handle with insufficient buffer space, **WriteFile** returns **TRUE** with *\*lpNumberOfBytesWritten* &lt; *nNumberOfBytesToWrite*.

For more information about pipes, see [Pipes](/windows/win32/ipc/pipes).

#### Transacted Operations

If there is a transaction bound to the file handle, then the file write is transacted. For more information, see [About Transactional NTFS](/windows/win32/FileIO/about-transactional-ntfs).

#### Examples

For some examples, see [Creating and Using a Temporary File](/windows/win32/FileIO/creating-and-using-a-temporary-file) and [Opening a File for Reading or Writing](/windows/win32/FileIO/opening-a-file-for-reading-or-writing).

The following C++ example shows how to align sectors for unbuffered file writes. The *Size* variable is the size of the original data block you are interested in writing to the file. For additional rules regarding unbuffered file I/O, see [File Buffering](/windows/win32/FileIO/file-buffering).

```cpp
#include <windows.h>

#define ROUND_UP_SIZE(Value,Pow2) ((SIZE_T) ((((ULONG)(Value)) + (Pow2) - 1) & (~(((LONG)(Pow2)) - 1))))
#define ROUND_UP_PTR(Ptr,Pow2)  ((void *) ((((ULONG_PTR)(Ptr)) + (Pow2) - 1) & (~(((LONG_PTR)(Pow2)) - 1))))

int main()
{
   // Sample data
   unsigned long bytesPerSector = 65536; // obtained from the GetFreeDiskSpace function.
   unsigned long size = 15536; // Buffer size of your data to write.
   
   // Ensure you have one more sector than Size would require.
   size_t sizeNeeded = bytesPerSector + ROUND_UP_SIZE(size, bytesPerSector);
   
   // Replace this statement with any allocation routine.
   auto buffer = new uint8_t[sizeNeeded];
   
   // Actual alignment happens here.
   auto bufferAligned = ROUND_UP_PTR(buffer, bytesPerSector);

   // ... Add code using bufferAligned here.
   
   // Replace with corresponding free routine.
   delete buffer;
}

```

## -see-also

[CancelIo](/windows/win32/FileIO/cancelio)

[CancelIoEx](/windows/win32/FileIO/cancelioex-func)

[CancelSynchronousIo](/windows/win32/FileIO/cancelsynchronousio-func)

[CreateFile](nf-fileapi-createfilea.md)

[CreateFileTransacted](/windows/win32/api/winbase/nf-winbase-createfiletransacteda)

[File Management Functions](/windows/win32/FileIO/file-management-functions)

[GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

[GetOverlappedResult](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult)

[GetQueuedCompletionStatus](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

[ReadFile](nf-fileapi-readfile.md)

[SetEndOfFile](nf-fileapi-setendoffile.md)

[WriteFileEx](nf-fileapi-writefileex.md)
