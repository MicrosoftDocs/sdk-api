---
UID: NI:winioctl.IOCTL_DISK_IS_WRITABLE
title: IOCTL_DISK_IS_WRITABLE
description: Determines whether the specified disk is writable.
helpviewer_keywords: ["IOCTL_DISK_IS_WRITABLE","IOCTL_DISK_IS_WRITABLE control","IOCTL_DISK_IS_WRITABLE control code [Files]","base.ioctl_disk_is_writable","fs.ioctl_disk_is_writable","winioctl/IOCTL_DISK_IS_WRITABLE"]
old-location: fs\ioctl_disk_is_writable.htm
tech.root: fs
ms.assetid: 0b56ea0d-95ae-4306-9866-b4b5e985ed43
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_IS_WRITABLE, IOCTL_DISK_IS_WRITABLE control, IOCTL_DISK_IS_WRITABLE control code [Files], base.ioctl_disk_is_writable, fs.ioctl_disk_is_writable, winioctl/IOCTL_DISK_IS_WRITABLE
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
 - IOCTL_DISK_IS_WRITABLE
 - winioctl/IOCTL_DISK_IS_WRITABLE
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
 - IOCTL_DISK_IS_WRITABLE
---

# IOCTL_DISK_IS_WRITABLE IOCTL


## -description

Determines whether the specified disk is writable.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_DISK_IS_WRITABLE,       // dwIoControlCode
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

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)