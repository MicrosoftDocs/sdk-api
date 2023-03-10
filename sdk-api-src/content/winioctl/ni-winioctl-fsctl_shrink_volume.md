---
UID: NI:winioctl.FSCTL_SHRINK_VOLUME
title: FSCTL_SHRINK_VOLUME
description: Signals that the volume is to be prepared to perform the shrink operation, the shrink operation is to be committed, or the shrink operation is to be terminated.
helpviewer_keywords: ["FSCTL_SHRINK_VOLUME","FSCTL_SHRINK_VOLUME control","FSCTL_SHRINK_VOLUME control code [Files]","fs.fsctl_shrink_volume","winioctl/FSCTL_SHRINK_VOLUME"]
old-location: fs\fsctl_shrink_volume.htm
tech.root: fs
ms.assetid: cf545417-f933-4054-bed4-e6adbf822f9c
ms.date: 12/05/2018
ms.keywords: FSCTL_SHRINK_VOLUME, FSCTL_SHRINK_VOLUME control, FSCTL_SHRINK_VOLUME control code [Files], fs.fsctl_shrink_volume, winioctl/FSCTL_SHRINK_VOLUME
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FSCTL_SHRINK_VOLUME
 - winioctl/FSCTL_SHRINK_VOLUME
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
 - FSCTL_SHRINK_VOLUME
---

# FSCTL_SHRINK_VOLUME IOCTL


## -description

Signals that the volume is to be prepared to perform the shrink operation, the shrink operation is to be committed, or the shrink operation is to be terminated.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SHRINK_VOLUME,          // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  nInBufferSize,                // size of input buffer    
  NULL,                         // output buffer
  O,                            // size of output buffer
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

This control code is only supported on NTFS and RAW file systems.

To complete a shrink operation, you must: 
1. Call [CreateFile](../fileapi/nf-fileapi-createfilea.md) to open a handle to the volume.
1. Call **FSCTL_SHRINK_VOLUME**. Set the **ShrinkRequestType** member of the [SHRINK_VOLUME_INFORMATION](ns-winioctl-shrink_volume_information.md) structure to **ShrinkPrepare**. Set the **NewNumberOfSectors** member of the same structure to zero.  If this call succeeds, the filesystem will not allocate clusters beyond the end of the new volume length.
1. Call [FSCTL_MOVE_FILE](ni-winioctl-fsctl_move_file.md) on all files beyond the new number of sectors and move them within the valid range. You are responsible for moving any files that are affected by the shrink operation.
1. Call **FSCTL_SHRINK_VOLUME**.  Set the **ShrinkRequestType** member of the [SHRINK_VOLUME_INFORMATION](ns-winioctl-shrink_volume_information.md) structure to **ShrinkCommit**. Set the **NewNumberOfSectors** member of the same structure to zero. If all files beyond the end of the new volume size have not been moved, the call fails with **STATUS_ALREADY_COMMITTED** (**ERROR_ACCESS_DENIED**).  Otherwise, the filesystem has now been shrunk.
1. Call  [IOCTL_DISK_GROW_PARTITION](ni-winioctl-ioctl_disk_grow_partition.md). Set the **BytesToGrow** member of the [DISK_GROW_PARTITION](ns-winioctl-disk_grow_partition.md) structure to the negative number that represents the number of bytes to remove.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | See comment

Is supported only on the node that has NTFS mounted.

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_EXTEND_VOLUME](ni-winioctl-fsctl_extend_volume.md)
* [IOCTL_DISK_GROW_PARTITION](ni-winioctl-ioctl_disk_grow_partition.md)
* [SHRINK_VOLUME_INFORMATION](ns-winioctl-shrink_volume_information.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)