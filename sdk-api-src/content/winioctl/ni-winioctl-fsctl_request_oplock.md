---
UID: NI:winioctl.FSCTL_REQUEST_OPLOCK
title: FSCTL_REQUEST_OPLOCK
description: Requests an opportunistic lock (oplock) on a file and acknowledges that an oplock break has occurred.
helpviewer_keywords: ["FSCTL_REQUEST_OPLOCK","FSCTL_REQUEST_OPLOCK control","FSCTL_REQUEST_OPLOCK control code [Files]","fs.fsctl_request_oplock","winioctl/FSCTL_REQUEST_OPLOCK"]
old-location: fs\fsctl_request_oplock.htm
tech.root: fs
ms.assetid: 9df94089-137a-4540-9f46-119408b362ba
ms.date: 01/23/2025
ms.keywords: FSCTL_REQUEST_OPLOCK, FSCTL_REQUEST_OPLOCK control, FSCTL_REQUEST_OPLOCK control code [Files], fs.fsctl_request_oplock, winioctl/FSCTL_REQUEST_OPLOCK
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
f1_keywords:
 - FSCTL_REQUEST_OPLOCK
 - winioctl/FSCTL_REQUEST_OPLOCK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_REQUEST_OPLOCK
---

# FSCTL_REQUEST_OPLOCK IOCTL


## -description

Requests an opportunistic lock (oplock) on a file and acknowledges that an oplock break has occurred.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function using the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to file
  FSCTL_REQUEST_OPLOCK,             // dwIoControlCode
  (LPVOID) lpInBuffer,              // pointer to REQUEST_OPLOCK_INPUT_BUFFER
  (DWORD) nInBufferSize,            // size of input buffer
  (LPVOID) lpOutBuffer,             // pointer to REQUEST_OPLOCK_OUTPUT_BUFFER
  (DWORD) nOutBufferSize,           // size of output buffer
  NULL,                             // number of bytes returned
  (LPOVERLAPPED) lpOverlapped       // OVERLAPPED structure
);
```

## -ioctlparameters

### -input-buffer

### -input-buffer-length

### -output-buffer

### -output-buffer-length

### -in-out-buffer

### -inout-buffer-length

### -status-block

## -remarks

This operation is used by client applications to request an opportunistic lock (oplock) from a local server. Client applications must not request opportunistic locks from remote servers directly—the network redirector transparently requests opportunistic locks for the application. Using this operation to request opportunistic locks from remote servers will result in the request being denied.

If the **DeviceIoControl** operation returns the error code **ERROR_IO_PENDING**, the oplock request has been granted. If it returns any other error code, the oplock has not been granted. If the error code is a warning value such as ERROR_CANNOT_GRANT_REQUESTED_OPLOCK, extended information may be available in the [REQUEST_OPLOCK_OUTPUT_BUFFER](ns-winioctl-request_oplock_output_buffer.md) structure.

When a granted oplock breaks, the event object in the [**OVERLAPPED**](../minwinbase/ns-minwinbase-overlapped.md) structure will be signaled, and information will be returned in the [REQUEST_OPLOCK_OUTPUT_BUFFER](ns-winioctl-request_oplock_output_buffer.md) structure. The **Internal** member of the **OVERLAPPED** structure will be set to an NTSTATUS value that provides extended information about how the oplock broke.

OVERLAPPED.Internal value | Meaning |
--------------------------|---------|
STATUS_SUCCESS<br>0x0 | The oplock was broken by another file system operation. |
STATUS_OPLOCK_HANDLE_CLOSED<br>0x00000216 | The oplock is no longer in force because the file handle used to request it was closed. Note that if an oplock breaks because the handle that was used to request it was closed, there is no need to acknowledge the break, regardless of the oplock type. |
STATUS_OPLOCK_SWITCHED_TO_NEW_HANDLE<br>0x00000215 | The oplock is still in force, however it is no longer associated with the file handle that was used to request it. A caller used a different handle to the file to request a new oplock, and that handle now owns the oplock. |

The **FSCTL_REQUEST_OPLOCK** control code provides more efficient functionality than the following related control codes: [FSCTL_REQUEST_OPLOCK_LEVEL_1](ni-winioctl-fsctl_request_oplock_level_1.md), [FSCTL_REQUEST_OPLOCK_LEVEL_2](ni-winioctl-fsctl_request_oplock_level_2.md), [FSCTL_REQUEST_FILTER_OPLOCK](ni-winioctl-fsctl_request_filter_oplock.md), and [FSCTL_REQUEST_BATCH_OPLOCK](ni-winioctl-fsctl_request_batch_oplock.md). Requesting different oplock levels can be performed repeatedly on the same handle without closing and reopening the handle when using **FSCTL_REQUEST_OPLOCK**; the other control codes require that the handle be closed and then reopened with [CreateFile](../fileapi/nf-fileapi-createfilea.md) to make such a change. This is accomplished by manipulating the **RequestedOplockLevel** member of the [REQUEST_OPLOCK_INPUT_BUFFER](ns-winioctl-request_oplock_input_buffer.md) structure when re-issuing the **FSCTL_REQUEST_OPLOCK** control code.

The following table summarizes how the caching ability of oplock types available from **FSCTL_REQUEST_OPLOCK** correspond to the level 2, level 1, and batch oplocks.

Alternative control code | Equivalent **RequestedOplockLevel** flags value | Oplock type
-------------------------|-------------------------------------------------|------------
[FSCTL_REQUEST_BATCH_OPLOCK](ni-winioctl-fsctl_request_batch_oplock.md) | `OPLOCK_LEVEL_CACHE_READ \| OPLOCK_LEVEL_CACHE_WRITE \| OPLOCK_LEVEL_CACHE_HANDLE` | RWH
[FSCTL_REQUEST_OPLOCK_LEVEL_1](ni-winioctl-fsctl_request_oplock_level_1.md) | `OPLOCK_LEVEL_CACHE_READ \| OPLOCK_LEVEL_CACHE_WRITE` | RW
[FSCTL_REQUEST_OPLOCK_LEVEL_2](ni-winioctl-fsctl_request_oplock_level_2.md) | `OPLOCK_LEVEL_CACHE_READ` | R

 

Using the **FSCTL_REQUEST_OPLOCK** control code with the **RequestedOplockLevel** member set to `OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_HANDLE` grants an oplock of type *RH*. An RH oplock is similar to the filter oplock granted by the [FSCTL_REQUEST_FILTER_OPLOCK](ni-winioctl-fsctl_request_filter_oplock.md) control code. However, note that the filter oplock allows only one client to hold an oplock on a file at a time; **FSCTL_REQUEST_OPLOCK** allows multiple clients at a time to have the *RH* lock on a file. Another difference is that **FSCTL_REQUEST_FILTER_OPLOCK** requires an oplock break acknowledgment before writes can occur, where **FSCTL_REQUEST_OPLOCK** does not because the oplock break notification is advisory-only and writes are allowed to go ahead without acknowledgment. For more information, see [Breaking Oplocks](/windows-hardware/drivers/ifs/breaking-oplocks).

An **FSCTL_REQUEST_OPLOCK** control code fails if the file is opened in non-overlapped (synchronous) mode.

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | Yes

 

Also, beginning in Windows 8 and Windows Server 2012, the **FSCTL_REQUEST_OPLOCK** control code can be used to request an oplock on a directory as well as a file. An oplock request on a directory may specify either `OPLOCK_LEVEL_CACHE_READ` or `OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_HANDLE` in the RequestedOplockLevel member.

An R or RH oplock on a directory breaks to None when the contents of an enumeration of the directory would change. For example, adding/deleting a file in the directory, changing the size of a file in the directory, modifying the timestamp of a file in the directory, etc., would all break the oplock on the directory. This oplock break does not require an acknowledgment before the changes in the directory may occur; it is advisory-only.

An RH oplock on a directory breaks to R when the directory itself is renamed or deleted. This oplock break does require an acknowledgment before the change to the directory can occur.

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [Oplock Semantics](/windows-hardware/drivers/ifs/oplock-semantics)
* [Opportunistic Locks](/windows/desktop/FileIO/opportunistic-locks)