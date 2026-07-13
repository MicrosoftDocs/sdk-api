---
UID: NI:winioctl.IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS
title: IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS
description: Initializes the status of all elements or the specified elements of a particular type.
helpviewer_keywords: ["IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS","IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS control","IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS control code","_win32_ioctl_changer_initialize_element_status","base.ioctl_changer_initialize_element_status","winioctl/IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS"]
old-location: base\ioctl_changer_initialize_element_status.htm
tech.root: base
ms.assetid: be054a22-cde4-4efd-bd66-eb67b007fd19
ms.date: 12/05/2018
ms.keywords: IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS, IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS control, IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS control code, _win32_ioctl_changer_initialize_element_status, base.ioctl_changer_initialize_element_status, winioctl/IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS
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
 - IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS
 - winioctl/IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS
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
 - IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS
---

# IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS IOCTL


## -description

Initializes the status of all elements or the specified elements of a particular type.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                         // handle to device
  IOCTL_CHANGER_INITIALIZE_ELEMENT_STATUS,  // dwIoControlCode
  (LPVOID) lpInBuffer,                      // input buffer
  (DWORD) nInBufferSize,                    // size of input buffer
  NULL,                                     // lpOutBuffer
  0,                                        // nOutBufferSize
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

* [CHANGER_INITIALIZE_ELEMENT_STATUS](ns-winioctl-changer_initialize_element_status.md)
* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)