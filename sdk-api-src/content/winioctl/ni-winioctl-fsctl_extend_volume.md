---
UID: NI:winioctl.FSCTL_EXTEND_VOLUME
title: FSCTL_EXTEND_VOLUME
description: Increases the size of a mounted volume.
helpviewer_keywords: ["FSCTL_EXTEND_VOLUME","FSCTL_EXTEND_VOLUME control","FSCTL_EXTEND_VOLUME control code [Files]","base.fsctl_extend_volume","fs.fsctl_extend_volume","winioctl/FSCTL_EXTEND_VOLUME"]
old-location: fs\fsctl_extend_volume.htm
tech.root: fs
ms.assetid: b941c5c8-39b4-4a5d-93e9-acbde7177d44
ms.date: 12/05/2018
ms.keywords: FSCTL_EXTEND_VOLUME, FSCTL_EXTEND_VOLUME control, FSCTL_EXTEND_VOLUME control code [Files], base.fsctl_extend_volume, fs.fsctl_extend_volume, winioctl/FSCTL_EXTEND_VOLUME
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
 - FSCTL_EXTEND_VOLUME
 - winioctl/FSCTL_EXTEND_VOLUME
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
 - FSCTL_EXTEND_VOLUME
---

# FSCTL_EXTEND_VOLUME IOCTL


## -description

Increases the size of a mounted volume.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_EXTEND_VOLUME,          // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
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

This control code is supported on NTFS, RAW, and ReFS file systems.

This control code cannot be used to reduce the size of a volume. The new volume size must be at least one cluster larger than the previous volume size. The underlying partition must have enough sectors to contain the extended volume. If not, [IOCTL_DISK_GROW_PARTITION](ni-winioctl-ioctl_disk_grow_partition.md) can be used if the underlying device has enough space available.

You can extend a live volume, and the volume can be open for sharing during the extend operation.

You do not need to lock a volume that you are extending, nor do you need to shut down other applications or services during the extend operation.

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
* [FSCTL_SHRINK_VOLUME](ni-winioctl-fsctl_shrink_volume.md)
* [IOCTL_DISK_GROW_PARTITION](ni-winioctl-ioctl_disk_grow_partition.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)