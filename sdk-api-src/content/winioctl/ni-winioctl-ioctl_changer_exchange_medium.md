---
UID: NI:winioctl.IOCTL_CHANGER_EXCHANGE_MEDIUM
title: IOCTL_CHANGER_EXCHANGE_MEDIUM
description: Moves a piece of media from a source element to one destination, and the piece of media originally in the first destination to a second destination.
helpviewer_keywords: ["IOCTL_CHANGER_EXCHANGE_MEDIUM","IOCTL_CHANGER_EXCHANGE_MEDIUM control","IOCTL_CHANGER_EXCHANGE_MEDIUM control code","_win32_ioctl_changer_exchange_medium","base.ioctl_changer_exchange_medium","winioctl/IOCTL_CHANGER_EXCHANGE_MEDIUM"]
old-location: base\ioctl_changer_exchange_medium.htm
tech.root: base
ms.assetid: 40550df0-9da4-4b02-bd57-23eae78c68df
ms.date: 12/05/2018
ms.keywords: IOCTL_CHANGER_EXCHANGE_MEDIUM, IOCTL_CHANGER_EXCHANGE_MEDIUM control, IOCTL_CHANGER_EXCHANGE_MEDIUM control code, _win32_ioctl_changer_exchange_medium, base.ioctl_changer_exchange_medium, winioctl/IOCTL_CHANGER_EXCHANGE_MEDIUM
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
 - IOCTL_CHANGER_EXCHANGE_MEDIUM
 - winioctl/IOCTL_CHANGER_EXCHANGE_MEDIUM
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
 - IOCTL_CHANGER_EXCHANGE_MEDIUM
---

# IOCTL_CHANGER_EXCHANGE_MEDIUM IOCTL


## -description

Moves a piece of media from a source element to one destination, and the piece of media originally in the first destination to a second destination.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_CHANGER_EXCHANGE_MEDIUM,    // dwIoControlCode
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

To swap two pieces of media, specify the source as the value for the second destination.

## -see-also

* [CHANGER_EXCHANGE_MEDIUM](ns-winioctl-changer_exchange_medium.md)
* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)