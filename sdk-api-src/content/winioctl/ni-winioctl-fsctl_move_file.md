---
UID: NI:winioctl.FSCTL_MOVE_FILE
title: FSCTL_MOVE_FILE
description: Relocates one or more virtual clusters of a file from one logical cluster to another within the same volume. This operation is used during defragmentation.
helpviewer_keywords: ["FSCTL_MOVE_FILE","FSCTL_MOVE_FILE control","FSCTL_MOVE_FILE control code [Files]","_win32_fsctl_move_file","base.fsctl_move_file","fs.fsctl_move_file","winioctl/FSCTL_MOVE_FILE"]
old-location: fs\fsctl_move_file.htm
tech.root: fs
ms.assetid: ab7f81ac-a962-4e86-b426-b0082d251645
ms.date: 12/05/2018
ms.keywords: FSCTL_MOVE_FILE, FSCTL_MOVE_FILE control, FSCTL_MOVE_FILE control code [Files], _win32_fsctl_move_file, base.fsctl_move_file, fs.fsctl_move_file, winioctl/FSCTL_MOVE_FILE
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
 - FSCTL_MOVE_FILE
 - winioctl/FSCTL_MOVE_FILE
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
 - FSCTL_MOVE_FILE
---

# FSCTL_MOVE_FILE IOCTL


## -description

Relocates one or more virtual clusters of a file from one logical cluster to another within the same volume. This operation is used during [defragmentation](/windows/desktop/FileIO/defragmenting-files).

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to volume
  FSCTL_MOVE_FILE,              // dwIoControlCode
  (LPVOID) lpInBuffer,          // MOVE_FILE_DATA structure
  (DWORD) nInBufferSize,        // size of input buffer
  NULL,                         // lpOutBuffer
  0,                            // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
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

The **FSCTL_MOVE_FILE** control code relocates one or more virtual clusters of a file from one logical cluster to another within the same volume. If the file to be moved is a sparse or compressed file, the granularity of the move is 16 clusters; otherwise, the granularity is one cluster.

To mark an open  file so that it is not defragmented, call the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the [FSCTL_MARK_HANDLE](ni-winioctl-fsctl_mark_handle.md) control code with **MARK_HANDLE_PROTECT_CLUSTERS** in the **HandleInfo** member of the [MARK_HANDLE_INFO](ns-winioctl-mark_handle_info.md) structure passed in the *lpInBuffer* parameter.

Note that the bitmap returned by the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the [FSCTL_GET_VOLUME_BITMAP](ni-winioctl-fsctl_get_volume_bitmap.md) control code represents a point in time, and can be incorrect as soon as it has been read if the volume has write activity. Thus, it is possible to attempt to move a cluster onto an allocated cluster in spite of a recent bitmap indicating that the cluster is unallocated. Programs using **FSCTL_MOVE_FILE** must be prepared for this possibility.

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

For a list of files, streams, and stream types supported by the **FSCTL_MOVE_FILE** control code, see the [Files, streams, and stream types supported for defragmentation](/windows/win32/fileio/defragmenting-files#files-streams-and-stream-types-supported-for-defragmentation) section of the [Defragmenting Files](/windows/desktop/FileIO/defragmenting-files) topic.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [Defragmenting Files](/windows/desktop/FileIO/defragmenting-files)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [FSCTL_GET_VOLUME_BITMAP](ni-winioctl-fsctl_get_volume_bitmap.md)
* [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md)
* [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md)
* [GetQueuedCompletionStatus](../ioapiset/nf-ioapiset-getqueuedcompletionstatus.md)
* [MOVE_FILE_DATA](ns-winioctl-move_file_data.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)