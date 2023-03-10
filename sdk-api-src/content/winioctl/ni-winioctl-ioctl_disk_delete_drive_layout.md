---
UID: NI:winioctl.IOCTL_DISK_DELETE_DRIVE_LAYOUT
title: IOCTL_DISK_DELETE_DRIVE_LAYOUT
description: Removes the boot signature from the master boot record, so that the disk will be formatted from sector zero to the end of the disk.
helpviewer_keywords: ["IOCTL_DISK_DELETE_DRIVE_LAYOUT","IOCTL_DISK_DELETE_DRIVE_LAYOUT control","IOCTL_DISK_DELETE_DRIVE_LAYOUT control code [Files]","base.ioctl_disk_delete_drive_layout","fs.ioctl_disk_delete_drive_layout","winioctl/IOCTL_DISK_DELETE_DRIVE_LAYOUT"]
old-location: fs\ioctl_disk_delete_drive_layout.htm
tech.root: fs
ms.assetid: b790e1f8-9371-4ff9-a820-3ea1af29cc6b
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_DELETE_DRIVE_LAYOUT, IOCTL_DISK_DELETE_DRIVE_LAYOUT control, IOCTL_DISK_DELETE_DRIVE_LAYOUT control code [Files], base.ioctl_disk_delete_drive_layout, fs.ioctl_disk_delete_drive_layout, winioctl/IOCTL_DISK_DELETE_DRIVE_LAYOUT
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
 - IOCTL_DISK_DELETE_DRIVE_LAYOUT
 - winioctl/IOCTL_DISK_DELETE_DRIVE_LAYOUT
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
 - IOCTL_DISK_DELETE_DRIVE_LAYOUT
---

# IOCTL_DISK_DELETE_DRIVE_LAYOUT IOCTL


## -description

Removes the boot signature from the master boot record, so that the disk will be formatted from sector zero to the end of the disk. Partition information is no longer stored in sector zero.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_DELETE_DRIVE_LAYOUT,   // dwIoControlCode
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

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)