---
UID: NI:winioctl.IOCTL_STORAGE_CHECK_VERIFY
title: IOCTL_STORAGE_CHECK_VERIFY
description: Determines whether media are accessible for a device.
helpviewer_keywords: ["IOCTL_STORAGE_CHECK_VERIFY","IOCTL_STORAGE_CHECK_VERIFY control","IOCTL_STORAGE_CHECK_VERIFY control code","_win32_ioctl_storage_check_verify","base.ioctl_storage_check_verify","winioctl/IOCTL_STORAGE_CHECK_VERIFY"]
old-location: base\ioctl_storage_check_verify.htm
tech.root: base
ms.assetid: b4705882-30ce-4527-a1b5-c0b296b70274
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_CHECK_VERIFY, IOCTL_STORAGE_CHECK_VERIFY control, IOCTL_STORAGE_CHECK_VERIFY control code, _win32_ioctl_storage_check_verify, base.ioctl_storage_check_verify, winioctl/IOCTL_STORAGE_CHECK_VERIFY
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
 - IOCTL_STORAGE_CHECK_VERIFY
 - winioctl/IOCTL_STORAGE_CHECK_VERIFY
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
 - IOCTL_STORAGE_CHECK_VERIFY
---

# IOCTL_STORAGE_CHECK_VERIFY IOCTL


## -description

Determines whether media are accessible for a device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_STORAGE_CHECK_VERIFY,   // dwIoControlCode
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

* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)