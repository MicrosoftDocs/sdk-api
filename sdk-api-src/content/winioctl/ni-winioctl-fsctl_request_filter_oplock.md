---
UID: NI:winioctl.FSCTL_REQUEST_FILTER_OPLOCK
title: FSCTL_REQUEST_FILTER_OPLOCK
description: Requests a filter opportunistic lock on a file.
helpviewer_keywords: ["FSCTL_REQUEST_FILTER_OPLOCK","FSCTL_REQUEST_FILTER_OPLOCK control","FSCTL_REQUEST_FILTER_OPLOCK control code [Files]","_win32_fsctl_request_filter_oplock","base.fsctl_request_filter_oplock","fs.fsctl_request_filter_oplock","winioctl/FSCTL_REQUEST_FILTER_OPLOCK"]
old-location: fs\fsctl_request_filter_oplock.htm
tech.root: fs
ms.assetid: 112c5d30-2cfa-4a63-87f8-8d2e80ea33b0
ms.date: 12/05/2018
ms.keywords: FSCTL_REQUEST_FILTER_OPLOCK, FSCTL_REQUEST_FILTER_OPLOCK control, FSCTL_REQUEST_FILTER_OPLOCK control code [Files], _win32_fsctl_request_filter_oplock, base.fsctl_request_filter_oplock, fs.fsctl_request_filter_oplock, winioctl/FSCTL_REQUEST_FILTER_OPLOCK
req.header: winioctl.h
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
f1_keywords:
 - FSCTL_REQUEST_FILTER_OPLOCK
 - winioctl/FSCTL_REQUEST_FILTER_OPLOCK
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
 - FSCTL_REQUEST_FILTER_OPLOCK
---

# FSCTL_REQUEST_FILTER_OPLOCK IOCTL


## -description

Requests a filter opportunistic lock on a file.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function using the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to file
  FSCTL_REQUEST_FILTER_OPLOCK,      // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  NULL,                             // lpOutBuffer
  0,                                // nOutBufferSize
  (LPDWORD) lpBytesReturned,        // number of bytes returned
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

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

This operation is used only by client applications requesting an opportunistic lock from a local server. Client applications requesting opportunistic locks from remote servers must not request them directly—the network redirector transparently requests opportunistic locks for the application. An attempt to use this operation to request opportunistic locks from remote servers will result in the request being denied.

If a new oplock type is desired, the handle must be closed and a new handle reopened using [CreateFile](../fileapi/nf-fileapi-createfilea.md), and [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) must be called on the new handle with the desired **FSCTL_REQUEST_OPLOCK**_\_XXX_ control code. To request an oplock on a handle that can have the oplock type changed in place (the handle does not have to be closed and reopened), use the [FSCTL_REQUEST_OPLOCK](ni-winioctl-fsctl_request_oplock.md) control code.

Use **FSCTL_REQUEST_FILTER_OPLOCK** to request a filter opportunistic lock on a file. A client file system can cache read data and handle data locally as long as the filter lock is held, but only one client can hold the lock at a time.

The filter oplock owner must acknowledge an oplock break (see [Breaking opportunistic locks](/windows/win32/fileio/breaking-opportunistic-locks)) before any operation that is incompatible  with a filter oplock can go through on another handle. After the lock is broken, the network redirector is notified not to regard as valid any cached data from the file.

For more information, see [Types of Opportunistic Locks](/windows/desktop/FileIO/types-of-opportunistic-locks).

For a comparison of the various oplock control codes, see [FSCTL_REQUEST_OPLOCK](ni-winioctl-fsctl_request_oplock.md).

An **FSCTL_REQUEST_FILTER_OPLOCK** control code fails if the file is opened in non-overlapped (synchronous) mode.

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | Yes

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_REQUEST_OPLOCK](ni-winioctl-fsctl_request_oplock.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [Oplock Semantics](/windows-hardware/drivers/ifs/oplock-semantics)
* [Opportunistic Locks](/windows/desktop/FileIO/opportunistic-locks)