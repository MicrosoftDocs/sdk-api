---
UID: NI:winioctl.IOCTL_DISK_GET_DRIVE_GEOMETRY
title: IOCTL_DISK_GET_DRIVE_GEOMETRY
description: Retrieves information about the physical disk's geometry:\_type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.
old-location: fs\ioctl_disk_get_drive_geometry.htm
tech.root: FileIO
ms.assetid: 574efc29-112b-42fe-ad1b-72543f20e831
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_GEOMETRY, IOCTL_DISK_GET_DRIVE_GEOMETRY control, IOCTL_DISK_GET_DRIVE_GEOMETRY control code [Files], _win32_ioctl_disk_get_drive_geometry, base.ioctl_disk_get_drive_geometry, fs.ioctl_disk_get_drive_geometry, winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY
f1_keywords:
- winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY
dev_langs:
- c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- IOCTL_DISK_GET_DRIVE_GEOMETRY
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GET_DRIVE_GEOMETRY IOCTL

## -description

Retrieves information about the physical disk's geometry: type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.

> [!NOTE]
> **IOCTL_DISK_GET_DRIVE_GEOMETRY** has been superseded by [IOCTL_DISK_GET_DRIVE_GEOMETRY_EX IOCTL](ni-winioctl-ioctl_disk_get_drive_geometry_ex.md), which retrieves additional information.

To perform this operation, call the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to device
  IOCTL_DISK_GET_DRIVE_GEOMETRY, //dwIoControlCode
  NULL,                          //lpInBuffer
  0,                             // nInBufferSize
  (LPVOID) lpOutBuffer,          // output buffer
  (DWORD) nOutBufferSize,        // size of output buffer
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
);
```

## -parameters

### -param lpInBuffer [in, optional]

None

### -param nInBufferSize [in]

None


### -param lpOutBuffer [out, optional]

A pointer to the output buffer that is to receive the [DISK_GEOMETRY](https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-disk_geometry) data returned by the operation.

### -param nOutBufferSize [in]

The size of the output buffer, in bytes. It must be >= **sizeof**(DISK_GEOMETRY)

## -see-also

[DISK_GEOMETRY](https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-disk_geometry)

[DeviceIoControl](https://docs.microsoft.com/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)

[Disk Management Control Codes](https://docs.microsoft.com/windows/win32/FileIO/disk-management-control-codes)

[IOCTL_DISK_GET_DRIVE_GEOMETRY_EX](https://docs.microsoft.com/windows/win32/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry_ex)

[IOCTL_STORAGE_GET_MEDIA_TYPES](https://docs.microsoft.com/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_media_types)
