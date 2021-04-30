---
UID: NI:winioctl.IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
title: IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
description: Windows applications can use this control code to set the temperature threshold of a device (when it's supported by the device).
helpviewer_keywords: ["IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD","IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD control","IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD control code [Files]","fs.ioctl_storage_set_temperature_threshold","winioctl/IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD"]
old-location: fs\ioctl_storage_set_temperature_threshold.htm
tech.root: fs
ms.assetid: 6B4BF202-6CC9-4571-9078-019984805F00
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD, IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD control, IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD control code [Files], fs.ioctl_storage_set_temperature_threshold, winioctl/IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
 - IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
 - winioctl/IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoctl.h
api_name:
 - IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
---

# IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD IOCTL


## -description

Windows applications can use this control code to set the temperature threshold of a device (when it's supported by the device).  Use [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md) to determine if the device supports changing the over and under temperature thresholds.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                         // handle to device
  IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  // dwIoControlCode
  (LPDWORD) lpInBuffer,                     // input buffer
  (DWORD) nInBufferSize,                    // size of input buffer
  (LPDWORD) lpOutBuffer,                    // output buffer
  (DWORD) nOutBufferSize,                   // size of output buffer
  (LPDWORD) lpBytesReturned,                // number of bytes returned
  (LPOVERLAPPED) lpOverlapped               // OVERLAPPED structure
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
* [IOCTL_STORAGE_QUERY_PROPERTY](ni-winioctl-ioctl_storage_query_property.md)
* [STORAGE_PROPERTY_ID](ne-winioctl-storage_property_id.md)
* [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md)
* [STORAGE_TEMPERATURE_INFO](ns-winioctl-storage_temperature_info.md)
* [STORAGE_TEMPERATURE_THRESHOLD](ns-winioctl-storage_temperature_threshold.md)