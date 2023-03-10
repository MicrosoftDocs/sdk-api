---
UID: NI:winioctl.IOCTL_DISK_SET_DISK_ATTRIBUTES
title: IOCTL_DISK_SET_DISK_ATTRIBUTES
description: Sets the attributes of the specified disk device.
helpviewer_keywords: ["IOCTL_DISK_SET_DISK_ATTRIBUTES","IOCTL_DISK_SET_DISK_ATTRIBUTES control","IOCTL_DISK_SET_DISK_ATTRIBUTES control code [Files]","fs.ioctl_disk_set_disk_attributes","winioctl/IOCTL_DISK_SET_DISK_ATTRIBUTES"]
old-location: fs\ioctl_disk_set_disk_attributes.htm
tech.root: fs
ms.assetid: ba0e3666-8660-493c-b821-5997d577e7e2
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_SET_DISK_ATTRIBUTES, IOCTL_DISK_SET_DISK_ATTRIBUTES control, IOCTL_DISK_SET_DISK_ATTRIBUTES control code [Files], fs.ioctl_disk_set_disk_attributes, winioctl/IOCTL_DISK_SET_DISK_ATTRIBUTES
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IOCTL_DISK_SET_DISK_ATTRIBUTES
 - winioctl/IOCTL_DISK_SET_DISK_ATTRIBUTES
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
 - IOCTL_DISK_SET_DISK_ATTRIBUTES
---

# IOCTL_DISK_SET_DISK_ATTRIBUTES IOCTL


## -description

Sets the attributes of the specified disk device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_SET_DISK_ATTRIBUTES,   // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer: SET_DISK_ATTRIBUTES
  (DWORD) nInBufferSize,            // size of input buffer
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
* [IOCTL_DISK_GET_DISK_ATTRIBUTES](ni-winioctl-ioctl_disk_get_disk_attributes.md)
* [SET_DISK_ATTRIBUTES](ns-winioctl-set_disk_attributes.md)