---
UID: NI:winioctl.IOCTL_DISK_PERFORMANCE_OFF
title: IOCTL_DISK_PERFORMANCE_OFF
description: Disables the performance counters that provide disk performance information.
helpviewer_keywords: ["IOCTL_DISK_PERFORMANCE_OFF","IOCTL_DISK_PERFORMANCE_OFF control","IOCTL_DISK_PERFORMANCE_OFF control code [Files]","base.ioctl_disk_performance_off","fs.ioctl_disk_performance_off","winioctl/IOCTL_DISK_PERFORMANCE_OFF"]
old-location: fs\ioctl_disk_performance_off.htm
tech.root: fs
ms.assetid: 68f4f6fb-a4f3-4fa5-8187-b2287a4271e8
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_PERFORMANCE_OFF, IOCTL_DISK_PERFORMANCE_OFF control, IOCTL_DISK_PERFORMANCE_OFF control code [Files], base.ioctl_disk_performance_off, fs.ioctl_disk_performance_off, winioctl/IOCTL_DISK_PERFORMANCE_OFF
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
 - IOCTL_DISK_PERFORMANCE_OFF
 - winioctl/IOCTL_DISK_PERFORMANCE_OFF
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
 - IOCTL_DISK_PERFORMANCE_OFF
---

# IOCTL_DISK_PERFORMANCE_OFF IOCTL


## -description

Disables the performance counters that provide disk performance information.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,            	// handle to device
  IOCTL_DISK_PERFORMANCE_OFF,	// dwIoControlCode
  NULL,                        	// lpInBuffer
  0,                           	// nInBufferSize
  NULL,                        	// lpOutBuffer
  0,                           	// nOutBufferSize
  (LPDWORD) lpBytesReturned,   	// number of bytes returned
  (LPOVERLAPPED) lpOverlapped  	// OVERLAPPED structure
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

To enable these performance counters, use the [IOCTL_DISK_PERFORMANCE](ni-winioctl-ioctl_disk_performance.md) control code.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [IOCTL_DISK_PERFORMANCE](ni-winioctl-ioctl_disk_performance.md)