---
UID: NI:winioctl.IOCTL_STORAGE_GET_HOTPLUG_INFO
title: IOCTL_STORAGE_GET_HOTPLUG_INFO
description: Retrieves the hotplug configuration of the specified device.
helpviewer_keywords: ["IOCTL_STORAGE_GET_HOTPLUG_INFO","IOCTL_STORAGE_GET_HOTPLUG_INFO control","IOCTL_STORAGE_GET_HOTPLUG_INFO control code","_win32_ioctl_storage_get_hotplug_info","base.ioctl_storage_get_hotplug_info","winioctl/IOCTL_STORAGE_GET_HOTPLUG_INFO"]
old-location: base\ioctl_storage_get_hotplug_info.htm
tech.root: base
ms.assetid: 4ecf6f84-17fc-4c48-a859-c043e8f9cd14
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_GET_HOTPLUG_INFO, IOCTL_STORAGE_GET_HOTPLUG_INFO control, IOCTL_STORAGE_GET_HOTPLUG_INFO control code, _win32_ioctl_storage_get_hotplug_info, base.ioctl_storage_get_hotplug_info, winioctl/IOCTL_STORAGE_GET_HOTPLUG_INFO
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
 - IOCTL_STORAGE_GET_HOTPLUG_INFO
 - winioctl/IOCTL_STORAGE_GET_HOTPLUG_INFO
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
 - IOCTL_STORAGE_GET_HOTPLUG_INFO
---

# IOCTL_STORAGE_GET_HOTPLUG_INFO IOCTL


## -description

Retrieves the hotplug configuration of the specified device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_STORAGE_GET_HOTPLUG_INFO,   // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  (LPVOID) lpOutBuffer,             // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
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

Refer to the Remarks section in the reference page for [STORAGE_HOTPLUG_INFO](ns-winioctl-storage_hotplug_info.md) for more information about hotplug devices.

## -see-also

* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [IOCTL_STORAGE_SET_HOTPLUG_INFO](ni-winioctl-ioctl_storage_set_hotplug_info.md)
* [STORAGE_HOTPLUG_INFO](ns-winioctl-storage_hotplug_info.md)