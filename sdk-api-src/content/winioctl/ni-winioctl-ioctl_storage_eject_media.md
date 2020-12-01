---
UID: NI:winioctl.IOCTL_STORAGE_EJECT_MEDIA
title: IOCTL_STORAGE_EJECT_MEDIA
description: Ejects media from a SCSI device.
helpviewer_keywords: ["IOCTL_STORAGE_EJECT_MEDIA","IOCTL_STORAGE_EJECT_MEDIA control","IOCTL_STORAGE_EJECT_MEDIA control code","_win32_ioctl_storage_eject_media","base.ioctl_storage_eject_media","winioctl/IOCTL_STORAGE_EJECT_MEDIA"]
old-location: base\ioctl_storage_eject_media.htm
tech.root: base
ms.assetid: e1eeb3b8-b52b-4570-a3bc-e245ae58464f
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_EJECT_MEDIA, IOCTL_STORAGE_EJECT_MEDIA control, IOCTL_STORAGE_EJECT_MEDIA control code, _win32_ioctl_storage_eject_media, base.ioctl_storage_eject_media, winioctl/IOCTL_STORAGE_EJECT_MEDIA
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
 - IOCTL_STORAGE_EJECT_MEDIA
 - winioctl/IOCTL_STORAGE_EJECT_MEDIA
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
 - IOCTL_STORAGE_EJECT_MEDIA
---

# IOCTL_STORAGE_EJECT_MEDIA IOCTL


## -description

Ejects media from a SCSI device.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_STORAGE_EJECT_MEDIA,    // dwIoControlCode
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

## -remarks

**IOCTL_STORAGE_EJECT_MEDIA** may or may not be supported on SCSI devices that support removable media.

## -see-also

* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [IOCTL_STORAGE_LOAD_MEDIA](ni-winioctl-ioctl_storage_load_media.md)
* [IOCTL_STORAGE_MEDIA_REMOVAL](ni-winioctl-ioctl_storage_media_removal.md)