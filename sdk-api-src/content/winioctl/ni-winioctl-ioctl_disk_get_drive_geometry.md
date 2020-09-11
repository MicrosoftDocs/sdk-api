---
UID: NI:winioctl.IOCTL_DISK_GET_DRIVE_GEOMETRY
title: IOCTL_DISK_GET_DRIVE_GEOMETRY
description: Retrieves information about the physical disk's geometry:\_type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.
helpviewer_keywords: ["IOCTL_DISK_GET_DRIVE_GEOMETRY","IOCTL_DISK_GET_DRIVE_GEOMETRY control","IOCTL_DISK_GET_DRIVE_GEOMETRY control code [Files]","_win32_ioctl_disk_get_drive_geometry","base.ioctl_disk_get_drive_geometry","fs.ioctl_disk_get_drive_geometry","winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY"]
old-location: fs\ioctl_disk_get_drive_geometry.htm
tech.root: fs
ms.assetid: 574efc29-112b-42fe-ad1b-72543f20e831
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_GEOMETRY, IOCTL_DISK_GET_DRIVE_GEOMETRY control, IOCTL_DISK_GET_DRIVE_GEOMETRY control code [Files], _win32_ioctl_disk_get_drive_geometry, base.ioctl_disk_get_drive_geometry, fs.ioctl_disk_get_drive_geometry, winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IOCTL_DISK_GET_DRIVE_GEOMETRY
 - winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY
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
 - IOCTL_DISK_GET_DRIVE_GEOMETRY
---

# IOCTL_DISK_GET_DRIVE_GEOMETRY IOCTL


## -description

Retrieves information about the physical disk's geometry: type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.

> [!NOTE]
> **IOCTL_DISK_GET_DRIVE_GEOMETRY** has been superseded by [**IOCTL_DISK_GET_DRIVE_GEOMETRY_EX**](ni-winioctl-ioctl_disk_get_drive_geometry_ex.md), which retrieves additional information.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_GET_DRIVE_GEOMETRY,    // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  (LPVOID) lpOutBuffer,             // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
  (LPDWORD) lpBytesReturned,        // number of bytes returned
  (LPOVERLAPPED) lpOverlapped       // OVERLAPPED structure
);
```

## -parameters

### -param hDevice [in]

A handle to the disk.

To retrieve a device handle, call the [**CreateFile**](../fileapi/nf-fileapi-createfilew.md) function.

### -param dwIoControlCode [in]

The control code for the operation.

Use **IOCTL_DISK_GET_DRIVE_GEOMETRY** for this operation.

### -param lpInBuffer [in, optional]

Not used with this operation. Set to **NULL**.

### -param nInBufferSize [in]

The size of the input buffer, in bytes. Set to 0 (zero).

### -param lpOutBuffer [out, optional]

A pointer to the output buffer that is to receive the [**DISK_GEOMETRY**](ns-winioctl-disk_geometry.md) data returned by the operation.

### -param nOutBufferSize [in]

The size of the output buffer, in bytes. It must be >= **sizeof**(DISK_GEOMETRY).

### -param lpBytesReturned [out, optional]

A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.

### -param lpOverlapped [in, out, optional]

A pointer to an [**OVERLAPPED**](../minwinbase/ns-minwinbase-overlapped.md) structure.

## -returns

If the operation completes successfully, the return value is nonzero.

If the operation fails or is pending, the return value is zero. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -see-also

* [DISK_GEOMETRY](ns-winioctl-disk_geometry.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/win32/FileIO/disk-management-control-codes)
* [IOCTL_DISK_GET_DRIVE_GEOMETRY_EX](ni-winioctl-ioctl_disk_get_drive_geometry_ex.md)
* [IOCTL_STORAGE_GET_MEDIA_TYPES](ni-winioctl-ioctl_storage_get_media_types.md)

