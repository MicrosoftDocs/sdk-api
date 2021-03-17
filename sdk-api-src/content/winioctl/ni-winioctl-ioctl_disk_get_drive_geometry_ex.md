---
UID: NI:winioctl.IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
title: IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
description: Retrieves extended information about the physical disk's geometry:\_type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.
helpviewer_keywords: ["IOCTL_DISK_GET_DRIVE_GEOMETRY_EX","IOCTL_DISK_GET_DRIVE_GEOMETRY_EX control","IOCTL_DISK_GET_DRIVE_GEOMETRY_EX control code [Files]","_win32_ioctl_disk_get_drive_geometry_ex","base.ioctl_disk_get_drive_geometry_ex","fs.ioctl_disk_get_drive_geometry_ex","winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY_EX"]
old-location: fs\ioctl_disk_get_drive_geometry_ex.htm
tech.root: fs
ms.assetid: 8a0667c8-b182-4851-af8e-411d95da0e3b
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_GEOMETRY_EX, IOCTL_DISK_GET_DRIVE_GEOMETRY_EX control, IOCTL_DISK_GET_DRIVE_GEOMETRY_EX control code [Files], _win32_ioctl_disk_get_drive_geometry_ex, base.ioctl_disk_get_drive_geometry_ex, fs.ioctl_disk_get_drive_geometry_ex, winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
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
 - IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
 - winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
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
 - IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
---

# IOCTL_DISK_GET_DRIVE_GEOMETRY_EX IOCTL


## -description

Retrieves extended information about the physical disk's geometry: type, number of cylinders, tracks per cylinder, sectors per track, bytes per sector, and size.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_GET_DRIVE_GEOMETRY_EX, // dwIoControlCode
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

Use **IOCTL_DISK_GET_DRIVE_GEOMETRY_EX** for this operation.

### -param lpInBuffer [in, optional]

Not used with this operation. Set to **NULL**.

### -param nInBufferSize [in]

The size of the input buffer, in bytes. Set to 0 (zero).

### -param lpOutBuffer [out, optional]

A pointer to the output buffer that is to receive the [**DISK_GEOMETRY_EX**](ns-winioctl-disk_geometry_ex.md) data returned by the operation.

If the size of the output buffer is (**sizeof**(DISK_GEOMETRY) + **sizeof**(LARGE_INTEGER)), the output buffer receives only [**DISK_GEOMETRY**](ns-winioctl-disk_geometry.md) data and disk size.

If you want to get [**DISK_PARTITION_INFO**](ns-winioctl-disk_partition_info.md) data and [**DISK_DETECTION_INFO**](ns-winioctl-disk_detection_info.md) data, the size of the output buffer must be at least (**sizeof**(DISK_GEOMETRY) + **sizeof**(LARGE_INTEGER) + **sizeof**(DISK_PARTITION_INFO) + **sizeof**(DISK_DETECTION_INFO)).

### -param nOutBufferSize [in]

The size of the output buffer, in bytes. It must be at least (**sizeof**(DISK_GEOMETRY) + **sizeof**(LARGE_INTEGER)).

### -param lpBytesReturned [out, optional]

A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.

### -param lpOverlapped [in, out, optional]

A pointer to an [**OVERLAPPED**](../minwinbase/ns-minwinbase-overlapped.md) structure.

## -returns

If the operation completes successfully, the return value is nonzero.

If the operation fails, or is pending, the return value is zero. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -see-also

* [DISK_GEOMETRY_EX](ns-winioctl-disk_geometry_ex.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/win32/FileIO/disk-management-control-codes)

