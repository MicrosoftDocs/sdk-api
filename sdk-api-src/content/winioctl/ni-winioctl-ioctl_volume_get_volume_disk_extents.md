---
UID: NI:winioctl.IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS
title: IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS
description: Retrieves the physical location of a specified volume on one or more disks.
helpviewer_keywords: ["IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS","IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS control","IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS control code [Files]","_win32_ioctl_volume_get_volume_disk_extents","base.ioctl_volume_get_volume_disk_extents","fs.ioctl_volume_get_volume_disk_extents","winioctl/IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS"]
old-location: fs\ioctl_volume_get_volume_disk_extents.htm
tech.root: fs
ms.assetid: 8faff037-d815-48f8-8b59-d63f4ff4a746
ms.date: 12/05/2018
ms.keywords: IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS control, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS control code [Files], _win32_ioctl_volume_get_volume_disk_extents, base.ioctl_volume_get_volume_disk_extents, fs.ioctl_volume_get_volume_disk_extents, winioctl/IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS
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
 - IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS
 - winioctl/IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS
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
 - IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS
---

# IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS IOCTL


## -description

Retrieves the physical location of a specified volume on one or more disks.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                     // handle to device
  IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, // dwIoControlCode
  NULL,                                 // lpInBuffer
  0,                                    // nInBufferSize
  (LPVOID) lpOutBuffer,                 // output buffer
  (DWORD) nOutBufferSize,               // size of output buffer
  (LPDWORD) lpBytesReturned,            // number of bytes returned
  (LPOVERLAPPED) lpOverlapped           // OVERLAPPED structure
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

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [VOLUME_DISK_EXTENTS](ns-winioctl-volume_disk_extents.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)