---
UID: NI:winioctl.IOCTL_DISK_UPDATE_PROPERTIES
title: IOCTL_DISK_UPDATE_PROPERTIES
description: Invalidates the cached partition table and re-enumerates the device.
helpviewer_keywords: ["IOCTL_DISK_UPDATE_PROPERTIES","IOCTL_DISK_UPDATE_PROPERTIES control","IOCTL_DISK_UPDATE_PROPERTIES control code [Files]","_win32_ioctl_disk_update_properties","base.ioctl_disk_update_properties","fs.ioctl_disk_update_properties","winioctl/IOCTL_DISK_UPDATE_PROPERTIES"]
old-location: fs\ioctl_disk_update_properties.htm
tech.root: fs
ms.assetid: d97e0257-c3b0-48d5-b801-594763be8178
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_UPDATE_PROPERTIES, IOCTL_DISK_UPDATE_PROPERTIES control, IOCTL_DISK_UPDATE_PROPERTIES control code [Files], _win32_ioctl_disk_update_properties, base.ioctl_disk_update_properties, fs.ioctl_disk_update_properties, winioctl/IOCTL_DISK_UPDATE_PROPERTIES
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
 - IOCTL_DISK_UPDATE_PROPERTIES
 - winioctl/IOCTL_DISK_UPDATE_PROPERTIES
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
 - IOCTL_DISK_UPDATE_PROPERTIES
---

# IOCTL_DISK_UPDATE_PROPERTIES IOCTL


## -description

Invalidates the cached partition table and re-enumerates the device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_DISK_UPDATE_PROPERTIES, // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  NULL,                         // lpOutBuffer
  0,                            // nOutBufferSize
  (LPDWORD)lpBytesReturned,     // lpBytesReturned
  (LPDWORD) lpOverlapped        // lpOverlapped
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

This operation is used in synchronizing the system view of the specified disk device when the partition table of the disk is directly modified. Be sure to perform this operation when you update the usable space for a disk so that the system will update its partition table.

You can update the properties of a live volume, and the volume can be open for sharing during the update operation.

You do not need to lock a volume that you are updating, nor do you need to shut down other applications or services during the update operation.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)