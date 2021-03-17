---
UID: NI:winioctl.FSCTL_GET_VOLUME_BITMAP
title: FSCTL_GET_VOLUME_BITMAP
description: Retrieves a bitmap of occupied and available clusters on a volume.
helpviewer_keywords: ["FSCTL_GET_VOLUME_BITMAP","FSCTL_GET_VOLUME_BITMAP control","FSCTL_GET_VOLUME_BITMAP control code [Files]","_win32_fsctl_get_volume_bitmap","base.fsctl_get_volume_bitmap","fs.fsctl_get_volume_bitmap","winioctl/FSCTL_GET_VOLUME_BITMAP"]
old-location: fs\fsctl_get_volume_bitmap.htm
tech.root: fs
ms.assetid: 80ef93ee-21a4-4766-82d2-d2ddef3ef5bb
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_VOLUME_BITMAP, FSCTL_GET_VOLUME_BITMAP control, FSCTL_GET_VOLUME_BITMAP control code [Files], _win32_fsctl_get_volume_bitmap, base.fsctl_get_volume_bitmap, fs.fsctl_get_volume_bitmap, winioctl/FSCTL_GET_VOLUME_BITMAP
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
 - FSCTL_GET_VOLUME_BITMAP
 - winioctl/FSCTL_GET_VOLUME_BITMAP
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
 - FSCTL_GET_VOLUME_BITMAP
---

# FSCTL_GET_VOLUME_BITMAP IOCTL


## -description

Retrieves a bitmap of occupied and available clusters on a volume.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to volume
  FSCTL_GET_VOLUME_BITMAP,      // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
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

The **FSCTL_GET_VOLUME_BITMAP** control code retrieves a data structure that describes the allocation state of each cluster in the file system from the requested starting LCN to the last cluster on the volume. The bitmap uses one bit to represent each cluster:
* The value 1 indicates that the cluster is allocated (in use).
* The value 0 indicates that the cluster is not allocated (free).

Note that the bitmap represents a point in time, and can be incorrect as soon as it has been read if the volume has write activity. Thus, it is possible to attempt to move a cluster onto an allocated cluster in spite of a recent bitmap indicating that the cluster is unallocated. Programs using the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the [FSCTL_MOVE_FILE](ni-winioctl-fsctl_move_file.md) control code must be prepared for this possibility.

The handle used here must be a Volume handle and have been opened with any access. Note that only Administrators can open Volume handles.

The starting LCN in the input buffer may be rounded down before the bitmap is calculated. The rounding limit is file system dependent.

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

This operation aligns the bitmap it returns on a page boundary.

**Windows Server 2003 and Windows XP:**  This operation aligns the bitmap it returns on a byte boundary.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [Defragmentation](/windows/desktop/FileIO/defragmenting-files)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [FSCTL_MOVE_FILE](ni-winioctl-fsctl_move_file.md)
* [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md)
* [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md)
* [GetQueuedCompletionStatus](../ioapiset/nf-ioapiset-getqueuedcompletionstatus.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [STARTING_LCN_INPUT_BUFFER](ns-winioctl-starting_lcn_input_buffer.md)
* [VOLUME_BITMAP_BUFFER](ns-winioctl-volume_bitmap_buffer.md)