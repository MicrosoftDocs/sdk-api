---
UID: NI:winioctl.IOCTL_STORAGE_EJECTION_CONTROL
title: IOCTL_STORAGE_EJECTION_CONTROL
description: Enables or disables the mechanism that ejects media. Disabling the mechanism locks the drive.
helpviewer_keywords: ["IOCTL_STORAGE_EJECTION_CONTROL","IOCTL_STORAGE_EJECTION_CONTROL control","IOCTL_STORAGE_EJECTION_CONTROL control code","_win32_ioctl_storage_ejection_control","base.ioctl_storage_ejection_control","winioctl/IOCTL_STORAGE_EJECTION_CONTROL"]
old-location: base\ioctl_storage_ejection_control.htm
tech.root: base
ms.assetid: d31aae7b-df93-419d-9a53-80a601a3c437
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_EJECTION_CONTROL, IOCTL_STORAGE_EJECTION_CONTROL control, IOCTL_STORAGE_EJECTION_CONTROL control code, _win32_ioctl_storage_ejection_control, base.ioctl_storage_ejection_control, winioctl/IOCTL_STORAGE_EJECTION_CONTROL
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
 - IOCTL_STORAGE_EJECTION_CONTROL
 - winioctl/IOCTL_STORAGE_EJECTION_CONTROL
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
 - IOCTL_STORAGE_EJECTION_CONTROL
---

# IOCTL_STORAGE_EJECTION_CONTROL IOCTL


## -description

Enables or disables the mechanism that ejects media. Disabling the mechanism locks the drive.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_STORAGE_EJECTION_CONTROL,   // dwIoControlCode
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

The driver tracks **IOCTL_STORAGE_EJECTION_CONTROL** requests by caller. It ignores requests to enable the ejection mechanism unless it has received a request to disable the ejection mechanism from the same caller. This prevents other callers from unlocking the drive.

## -see-also

* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [PREVENT_MEDIA_REMOVAL](ns-winioctl-prevent_media_removal.md)