---
UID: NI:winioctl.FSCTL_IS_VOLUME_MOUNTED
title: FSCTL_IS_VOLUME_MOUNTED
description: Determines whether the specified volume is mounted, or if the specified file or directory is on a mounted volume.
helpviewer_keywords: ["FSCTL_IS_VOLUME_MOUNTED","FSCTL_IS_VOLUME_MOUNTED control","FSCTL_IS_VOLUME_MOUNTED control code [Files]","base.fsctl_is_volume_mounted","fs.fsctl_is_volume_mounted","winioctl/FSCTL_IS_VOLUME_MOUNTED"]
old-location: fs\fsctl_is_volume_mounted.htm
tech.root: fs
ms.assetid: 1effd05a-2c9f-4c8b-97dd-ed93b04cc2ee
ms.date: 12/05/2018
ms.keywords: FSCTL_IS_VOLUME_MOUNTED, FSCTL_IS_VOLUME_MOUNTED control, FSCTL_IS_VOLUME_MOUNTED control code [Files], base.fsctl_is_volume_mounted, fs.fsctl_is_volume_mounted, winioctl/FSCTL_IS_VOLUME_MOUNTED
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
 - FSCTL_IS_VOLUME_MOUNTED
 - winioctl/FSCTL_IS_VOLUME_MOUNTED
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
 - FSCTL_IS_VOLUME_MOUNTED
---

# FSCTL_IS_VOLUME_MOUNTED IOCTL


## -description

Determines whether the specified volume is mounted, or if the specified file or directory is on a mounted volume.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_IS_VOLUME_MOUNTED,      // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
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

The NTFS file system treats a locked volume as a dismounted volume. Therefore, this call returns zero (0) after a volume is locked on the NTFS file system.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_DISMOUNT_VOLUME](ni-winioctl-fsctl_dismount_volume.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)