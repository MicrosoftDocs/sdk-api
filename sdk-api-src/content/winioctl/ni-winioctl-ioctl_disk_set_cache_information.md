---
UID: NI:winioctl.IOCTL_DISK_SET_CACHE_INFORMATION
title: IOCTL_DISK_SET_CACHE_INFORMATION
description: Sets the disk configuration data.
helpviewer_keywords: ["IOCTL_DISK_SET_CACHE_INFORMATION","IOCTL_DISK_SET_CACHE_INFORMATION control","IOCTL_DISK_SET_CACHE_INFORMATION control code [Files]","base.ioctl_disk_set_cache_information","fs.ioctl_disk_set_cache_information","winioctl/IOCTL_DISK_SET_CACHE_INFORMATION"]
old-location: fs\ioctl_disk_set_cache_information.htm
tech.root: fs
ms.assetid: e921da48-9435-41f0-87dd-abb383fd5208
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_SET_CACHE_INFORMATION, IOCTL_DISK_SET_CACHE_INFORMATION control, IOCTL_DISK_SET_CACHE_INFORMATION control code [Files], base.ioctl_disk_set_cache_information, fs.ioctl_disk_set_cache_information, winioctl/IOCTL_DISK_SET_CACHE_INFORMATION
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
 - IOCTL_DISK_SET_CACHE_INFORMATION
 - winioctl/IOCTL_DISK_SET_CACHE_INFORMATION
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
 - IOCTL_DISK_SET_CACHE_INFORMATION
---

# IOCTL_DISK_SET_CACHE_INFORMATION IOCTL


## -description

Sets the disk configuration data.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_SET_CACHE_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer
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

## -remarks

To retrieve the cache information, use the [IOCTL_DISK_GET_CACHE_INFORMATION](ni-winioctl-ioctl_disk_get_cache_information.md) control code.

## -see-also

* [DISK_CACHE_INFORMATION](ns-winioctl-disk_cache_information.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [IOCTL_DISK_GET_CACHE_INFORMATION](ni-winioctl-ioctl_disk_get_cache_information.md)