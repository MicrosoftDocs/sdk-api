---
UID: NI:winioctl.IOCTL_DISK_CREATE_DISK
title: IOCTL_DISK_CREATE_DISK
description: Initializes the specified disk and disk partition table using the information in the CREATE_DISK structure.
helpviewer_keywords: ["IOCTL_DISK_CREATE_DISK","IOCTL_DISK_CREATE_DISK control","IOCTL_DISK_CREATE_DISK control code [Files]","_win32_ioctl_disk_create_disk","base.ioctl_disk_create_disk","fs.ioctl_disk_create_disk","winioctl/IOCTL_DISK_CREATE_DISK"]
old-location: fs\ioctl_disk_create_disk.htm
tech.root: fs
ms.assetid: c8215a00-ea39-4268-bb66-68cf3d37baef
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_CREATE_DISK, IOCTL_DISK_CREATE_DISK control, IOCTL_DISK_CREATE_DISK control code [Files], _win32_ioctl_disk_create_disk, base.ioctl_disk_create_disk, fs.ioctl_disk_create_disk, winioctl/IOCTL_DISK_CREATE_DISK
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
 - IOCTL_DISK_CREATE_DISK
 - winioctl/IOCTL_DISK_CREATE_DISK
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
 - IOCTL_DISK_CREATE_DISK
---

# IOCTL_DISK_CREATE_DISK IOCTL


## -description

Initializes the specified disk and disk partition table using the information in the [CREATE_DISK](ns-winioctl-create_disk.md) structure.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_DISK_CREATE_DISK,       // dwIoControlCode
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

When specifying a GUID partition table (GPT) as the [PARTITION_STYLE](./ne-winioctl-partition_style.md) of the [CREATE_DISK](ns-winioctl-create_disk.md) structure, an application should wait for the MSR partition arrival before sending the [IOCTL_DISK_SET_DRIVE_LAYOUT_EX](ni-winioctl-ioctl_disk_set_drive_layout_ex.md) control code. For more information about device notification, see [RegisterDeviceNotification](../winuser/nf-winuser-registerdevicenotificationa.md).

## -see-also

* [CREATE_DISK](ns-winioctl-create_disk.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)