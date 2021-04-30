---
UID: NI:winioctl.IOCTL_CHANGER_SET_ACCESS
title: IOCTL_CHANGER_SET_ACCESS
description: Sets the state of the device's insert/eject port, door, or keypad.
helpviewer_keywords: ["IOCTL_CHANGER_SET_ACCESS","IOCTL_CHANGER_SET_ACCESS control","IOCTL_CHANGER_SET_ACCESS control code","_win32_ioctl_changer_set_access","base.ioctl_changer_set_access","winioctl/IOCTL_CHANGER_SET_ACCESS"]
old-location: base\ioctl_changer_set_access.htm
tech.root: base
ms.assetid: 567817d5-60cd-494c-94d9-0899e1142242
ms.date: 12/05/2018
ms.keywords: IOCTL_CHANGER_SET_ACCESS, IOCTL_CHANGER_SET_ACCESS control, IOCTL_CHANGER_SET_ACCESS control code, _win32_ioctl_changer_set_access, base.ioctl_changer_set_access, winioctl/IOCTL_CHANGER_SET_ACCESS
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
 - IOCTL_CHANGER_SET_ACCESS
 - winioctl/IOCTL_CHANGER_SET_ACCESS
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
 - IOCTL_CHANGER_SET_ACCESS
---

# IOCTL_CHANGER_SET_ACCESS IOCTL


## -description

Sets the state of the device's insert/eject port, door, or keypad.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_CHANGER_SET_ACCESS,     // dwIoControlCode
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

## -see-also

* [CHANGER_SET_ACCESS](ns-winioctl-changer_set_access.md)
* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)