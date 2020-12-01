---
UID: NI:winioctl.IOCTL_DISK_SET_DRIVE_LAYOUT_EX
title: IOCTL_DISK_SET_DRIVE_LAYOUT_EX
description: Partitions a disk according to the specified drive layout and partition information data.
helpviewer_keywords: ["IOCTL_DISK_SET_DRIVE_LAYOUT_EX","IOCTL_DISK_SET_DRIVE_LAYOUT_EX control","IOCTL_DISK_SET_DRIVE_LAYOUT_EX control code [Files]","_win32_ioctl_disk_set_drive_layout_ex","base.ioctl_disk_set_drive_layout_ex","fs.ioctl_disk_set_drive_layout_ex","winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT_EX"]
old-location: fs\ioctl_disk_set_drive_layout_ex.htm
tech.root: fs
ms.assetid: a600e841-c692-4aa4-bea2-a33931d9b007
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_SET_DRIVE_LAYOUT_EX, IOCTL_DISK_SET_DRIVE_LAYOUT_EX control, IOCTL_DISK_SET_DRIVE_LAYOUT_EX control code [Files], _win32_ioctl_disk_set_drive_layout_ex, base.ioctl_disk_set_drive_layout_ex, fs.ioctl_disk_set_drive_layout_ex, winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT_EX
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
 - IOCTL_DISK_SET_DRIVE_LAYOUT_EX
 - winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT_EX
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
 - IOCTL_DISK_SET_DRIVE_LAYOUT_EX
---

# IOCTL_DISK_SET_DRIVE_LAYOUT_EX IOCTL


## -description

Partitions a disk according to the specified drive layout and partition information data.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters. You must have write access to the drive in order to use this control code.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_SET_DRIVE_LAYOUT_EX,   // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
  NULL,                             // lpOutBuffer
  0,                                // nOutBufferSize
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

Use **IOCTL_DISK_SET_DRIVE_LAYOUT_EX** for this operation.

### -param lpInBuffer [in, optional]

A pointer to the input buffer that contains the [**DRIVE_LAYOUT_INFORMATION_EX**](ns-winioctl-drive_layout_information_ex.md) data to be set.

### -param nInBufferSize [in]

The size of the input buffer, in bytes. It must be >= **sizeof**(DRIVE_LAYOUT_INFORMATION_EX).

### -param lpOutBuffer [out, optional]

Not used with this operation. Set to **NULL**.

### -param nOutBufferSize [in]

The size of the input buffer, in bytes. Set to 0 (zero).

### -param lpBytesReturned [out, optional]

A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.

### -param lpOverlapped [in, out, optional]

A pointer to an [**OVERLAPPED**](../minwinbase/ns-minwinbase-overlapped.md) structure.

## -returns

If the operation completes successfully, the return value is nonzero.

If the operation fails or is pending, the return value is zero. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

When specifying a **GUID** partition table (GPT) as the [PARTITION_STYLE](ne-winioctl-partition_style.md) of the [CREATE_DISK](ns-winioctl-create_disk.md) structure, an application should wait for the MSR partition arrival before sending the **IOCTL_DISK_SET_DRIVE_LAYOUT_EX** control code. For more information about device notification, see [RegisterDeviceNotification](../winuser/nf-winuser-registerdevicenotificationa.md).

When creating and manipulating an Extended Boot Record (EBR), the first entry of the EBR should point to the logical drive that immediately follows the EBR and the next EBR should lie after the end of the current logical drive and before the start of the next logical drive.

If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of [IOCTL_DISK_SET_DRIVE_LAYOUT](ni-winioctl-ioctl_disk_set_drive_layout.md).

## -see-also

* [DRIVE_LAYOUT_INFORMATION_EX](ns-winioctl-drive_layout_information_ex.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/win32/FileIO/disk-management-control-codes)
* [IOCTL_DISK_GET_DRIVE_LAYOUT_EX](ni-winioctl-ioctl_disk_get_drive_layout_ex.md)

