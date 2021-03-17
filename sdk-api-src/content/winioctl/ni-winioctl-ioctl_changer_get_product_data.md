---
UID: NI:winioctl.IOCTL_CHANGER_GET_PRODUCT_DATA
title: IOCTL_CHANGER_GET_PRODUCT_DATA
description: Retrieves the product data for the specified device.
helpviewer_keywords: ["IOCTL_CHANGER_GET_PRODUCT_DATA","IOCTL_CHANGER_GET_PRODUCT_DATA control","IOCTL_CHANGER_GET_PRODUCT_DATA control code","_win32_ioctl_changer_get_product_data","base.ioctl_changer_get_product_data","winioctl/IOCTL_CHANGER_GET_PRODUCT_DATA"]
old-location: base\ioctl_changer_get_product_data.htm
tech.root: base
ms.assetid: 60744666-fb37-4263-8f4a-e7e043e6b71e
ms.date: 12/05/2018
ms.keywords: IOCTL_CHANGER_GET_PRODUCT_DATA, IOCTL_CHANGER_GET_PRODUCT_DATA control, IOCTL_CHANGER_GET_PRODUCT_DATA control code, _win32_ioctl_changer_get_product_data, base.ioctl_changer_get_product_data, winioctl/IOCTL_CHANGER_GET_PRODUCT_DATA
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
 - IOCTL_CHANGER_GET_PRODUCT_DATA
 - winioctl/IOCTL_CHANGER_GET_PRODUCT_DATA
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
 - IOCTL_CHANGER_GET_PRODUCT_DATA
---

# IOCTL_CHANGER_GET_PRODUCT_DATA IOCTL


## -description

Retrieves the product data for the specified device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_CHANGER_GET_PRODUCT_DATA,   // dwIoControlCode
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

## -see-also

* [CHANGER_PRODUCT_DATA](ns-winioctl-changer_product_data.md)
* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)