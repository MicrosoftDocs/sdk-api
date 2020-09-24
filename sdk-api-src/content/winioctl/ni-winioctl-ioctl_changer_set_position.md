---
UID: NI:winioctl.IOCTL_CHANGER_SET_POSITION
title: IOCTL_CHANGER_SET_POSITION
description: Sets the changer's robotic transport mechanism to the specified element address. This optimizes moving or exchanging media by positioning the transport beforehand.
helpviewer_keywords: ["IOCTL_CHANGER_SET_POSITION","IOCTL_CHANGER_SET_POSITION control","IOCTL_CHANGER_SET_POSITION control code","_win32_ioctl_changer_set_position","base.ioctl_changer_set_position","winioctl/IOCTL_CHANGER_SET_POSITION"]
old-location: base\ioctl_changer_set_position.htm
tech.root: base
ms.assetid: 1c3348d5-6d22-40cb-bf4f-e843819884b9
ms.date: 12/05/2018
ms.keywords: IOCTL_CHANGER_SET_POSITION, IOCTL_CHANGER_SET_POSITION control, IOCTL_CHANGER_SET_POSITION control code, _win32_ioctl_changer_set_position, base.ioctl_changer_set_position, winioctl/IOCTL_CHANGER_SET_POSITION
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
 - IOCTL_CHANGER_SET_POSITION
 - winioctl/IOCTL_CHANGER_SET_POSITION
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
 - IOCTL_CHANGER_SET_POSITION
---

# IOCTL_CHANGER_SET_POSITION IOCTL


## -description

Sets the changer's robotic transport mechanism to the specified element address. This optimizes moving or exchanging media by positioning the transport beforehand.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_CHANGER_SET_POSITION,   // dwIoControlCode
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

* [CHANGER_SET_POSITION](ns-winioctl-changer_set_position.md)
* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)