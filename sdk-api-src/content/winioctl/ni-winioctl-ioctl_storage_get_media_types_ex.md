---
UID: NI:winioctl.IOCTL_STORAGE_GET_MEDIA_TYPES_EX
title: IOCTL_STORAGE_GET_MEDIA_TYPES_EX
description: Retrieves information about the types of media supported by a device.
helpviewer_keywords: ["IOCTL_STORAGE_GET_MEDIA_TYPES_EX","IOCTL_STORAGE_GET_MEDIA_TYPES_EX control","IOCTL_STORAGE_GET_MEDIA_TYPES_EX control code","_win32_ioctl_storage_get_media_types_ex","base.ioctl_storage_get_media_types_ex","winioctl/IOCTL_STORAGE_GET_MEDIA_TYPES_EX"]
old-location: base\ioctl_storage_get_media_types_ex.htm
tech.root: base
ms.assetid: eb3676cb-9f50-4105-89b6-ee2174e197ec
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_GET_MEDIA_TYPES_EX, IOCTL_STORAGE_GET_MEDIA_TYPES_EX control, IOCTL_STORAGE_GET_MEDIA_TYPES_EX control code, _win32_ioctl_storage_get_media_types_ex, base.ioctl_storage_get_media_types_ex, winioctl/IOCTL_STORAGE_GET_MEDIA_TYPES_EX
f1_keywords:
- winioctl/IOCTL_STORAGE_GET_MEDIA_TYPES_EX
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinIoCtl.h
api_name:
- IOCTL_STORAGE_GET_MEDIA_TYPES_EX
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_GET_MEDIA_TYPES_EX IOCTL

## -description

Retrieves information about the types of media supported by a device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_STORAGE_GET_MEDIA_TYPES_EX, // dwIoControlCode
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).


## -see-also

* [Device Management Control Codes](https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [GET_MEDIA_TYPES](ns-winioctl-get_media_types.md)
