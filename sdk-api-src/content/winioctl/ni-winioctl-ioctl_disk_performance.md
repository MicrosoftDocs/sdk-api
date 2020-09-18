---
UID: NI:winioctl.IOCTL_DISK_PERFORMANCE
title: IOCTL_DISK_PERFORMANCE
description: Enables performance counters that provide disk performance information.
helpviewer_keywords: ["IOCTL_DISK_PERFORMANCE","IOCTL_DISK_PERFORMANCE control","IOCTL_DISK_PERFORMANCE control code [Files]","_win32_ioctl_disk_performance","base.ioctl_disk_performance","fs.ioctl_disk_performance","winioctl/IOCTL_DISK_PERFORMANCE"]
old-location: fs\ioctl_disk_performance.htm
tech.root: fs
ms.assetid: e182282c-17e9-442a-8742-437052cfed03
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_PERFORMANCE, IOCTL_DISK_PERFORMANCE control, IOCTL_DISK_PERFORMANCE control code [Files], _win32_ioctl_disk_performance, base.ioctl_disk_performance, fs.ioctl_disk_performance, winioctl/IOCTL_DISK_PERFORMANCE
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
 - IOCTL_DISK_PERFORMANCE
 - winioctl/IOCTL_DISK_PERFORMANCE
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
 - IOCTL_DISK_PERFORMANCE
---

# IOCTL_DISK_PERFORMANCE IOCTL


## -description

Enables performance counters that provide disk performance information.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_DISK_PERFORMANCE,       // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
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

To disable the  performance counters enabled by this control code, use the [IOCTL_DISK_PERFORMANCE_OFF](ni-winioctl-ioctl_disk_performance_off.md) control code.

## -see-also

* [DISK_PERFORMANCE](ns-winioctl-disk_performance.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [IOCTL_DISK_PERFORMANCE_OFF](ni-winioctl-ioctl_disk_performance_off.md)