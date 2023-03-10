---
UID: NI:winioctl.IOCTL_CHANGER_REINITIALIZE_TRANSPORT
title: IOCTL_CHANGER_REINITIALIZE_TRANSPORT
description: Physically recalibrates a transport element. Recalibration may involve returning the transport to its home position.
helpviewer_keywords: ["IOCTL_CHANGER_REINITIALIZE_TRANSPORT","IOCTL_CHANGER_REINITIALIZE_TRANSPORT control","IOCTL_CHANGER_REINITIALIZE_TRANSPORT control code","_win32_ioctl_changer_reinitialize_transport","base.ioctl_changer_reinitialize_transport","winioctl/IOCTL_CHANGER_REINITIALIZE_TRANSPORT"]
old-location: base\ioctl_changer_reinitialize_transport.htm
tech.root: base
ms.assetid: 0745ee19-34f3-44c8-a52d-fb47448f0084
ms.date: 12/05/2018
ms.keywords: IOCTL_CHANGER_REINITIALIZE_TRANSPORT, IOCTL_CHANGER_REINITIALIZE_TRANSPORT control, IOCTL_CHANGER_REINITIALIZE_TRANSPORT control code, _win32_ioctl_changer_reinitialize_transport, base.ioctl_changer_reinitialize_transport, winioctl/IOCTL_CHANGER_REINITIALIZE_TRANSPORT
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
 - IOCTL_CHANGER_REINITIALIZE_TRANSPORT
 - winioctl/IOCTL_CHANGER_REINITIALIZE_TRANSPORT
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
 - IOCTL_CHANGER_REINITIALIZE_TRANSPORT
---

# IOCTL_CHANGER_REINITIALIZE_TRANSPORT IOCTL


## -description

Physically recalibrates a transport element. Recalibration may involve returning the transport to its home position.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                     // handle to device
  IOCTL_CHANGER_REINITIALIZE_TRANSPORT, // dwIoControlCode
  (LPVOID) lpInBuffer,                  // input buffer
  (DWORD) nInBufferSize,                // size of input buffer
  NULL,                                 // lpOutBuffer
  0,                                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,            // number of bytes returned
  (LPOVERLAPPED) lpOverlapped           // OVERLAPPED structure
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

* [CHANGER_ELEMENT](ns-winioctl-changer_element.md)
* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)