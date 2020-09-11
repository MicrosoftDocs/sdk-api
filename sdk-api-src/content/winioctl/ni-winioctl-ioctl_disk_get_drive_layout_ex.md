---
UID: NI:winioctl.IOCTL_DISK_GET_DRIVE_LAYOUT_EX
title: IOCTL_DISK_GET_DRIVE_LAYOUT_EX
description: Retrieves extended information for each entry in the partition tables for a disk.
helpviewer_keywords: ["IOCTL_DISK_GET_DRIVE_LAYOUT_EX","IOCTL_DISK_GET_DRIVE_LAYOUT_EX control","IOCTL_DISK_GET_DRIVE_LAYOUT_EX control code [Files]","_win32_ioctl_disk_get_drive_layout_ex","base.ioctl_disk_get_drive_layout_ex","fs.ioctl_disk_get_drive_layout_ex","winioctl/IOCTL_DISK_GET_DRIVE_LAYOUT_EX"]
old-location: fs\ioctl_disk_get_drive_layout_ex.htm
tech.root: fs
ms.assetid: 21507182-5a33-4e58-b5ed-3724feefa4ed
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_LAYOUT_EX, IOCTL_DISK_GET_DRIVE_LAYOUT_EX control, IOCTL_DISK_GET_DRIVE_LAYOUT_EX control code [Files], _win32_ioctl_disk_get_drive_layout_ex, base.ioctl_disk_get_drive_layout_ex, fs.ioctl_disk_get_drive_layout_ex, winioctl/IOCTL_DISK_GET_DRIVE_LAYOUT_EX
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
 - IOCTL_DISK_GET_DRIVE_LAYOUT_EX
 - winioctl/IOCTL_DISK_GET_DRIVE_LAYOUT_EX
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
 - IOCTL_DISK_GET_DRIVE_LAYOUT_EX
---

# IOCTL_DISK_GET_DRIVE_LAYOUT_EX IOCTL


## -description

Retrieves extended information for each entry in the  partition tables for a disk.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters. You must have read access to the drive in order to use this control code.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_GET_DRIVE_LAYOUT_EX,   // dwIoControlCode
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

Use **IOCTL_DISK_GET_DRIVE_LAYOUT_EX** for this operation.

### -param lpInBuffer [in, optional]

Not used with this operation. Set to **NULL**.

### -param nInBufferSize [in]

The size of the input buffer, in bytes. Set to 0 (zero).

### -param lpOutBuffer [out, optional]

A pointer to the output buffer that is to receive the [**DRIVE_LAYOUT_INFORMATION_EX**](ns-winioctl-drive_layout_information_ex.md) data returned by the operation.

If the output buffer is not large enough to store the data, the function returns **FALSE** and [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md) returns **ERROR_INSUFFICIENT_BUFFER**.

### -param nOutBufferSize [in]

The size of the output buffer, in bytes. It must be >= **sizeof**(DRIVE_LAYOUT_INFORMATION_EX).

### -param lpBytesReturned [out, optional]

A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.

### -param lpOverlapped [in, out, optional]

A pointer to an [**OVERLAPPED**](../minwinbase/ns-minwinbase-overlapped.md) structure.

## -returns

If the operation completes successfully, the return value is nonzero.

If the operation fails or is pending, the return value is zero. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

This operation retrieves information for each primary partition as well as each logical drive. To determine whether the entry is an extended or unused partition, check the [Disk Partition Types](/windows/desktop/FileIO/disk-partition-types).

## -see-also

* [DRIVE_LAYOUT_INFORMATION_EX](ns-winioctl-drive_layout_information_ex.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/win32/FileIO/disk-management-control-codes)
* [IOCTL_DISK_SET_DRIVE_LAYOUT_EX](ni-winioctl-ioctl_disk_set_drive_layout_ex.md)

