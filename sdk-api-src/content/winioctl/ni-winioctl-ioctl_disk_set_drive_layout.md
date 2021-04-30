---
UID: NI:winioctl.IOCTL_DISK_SET_DRIVE_LAYOUT
title: IOCTL_DISK_SET_DRIVE_LAYOUT
description: Partitions a disk as specified by drive layout and partition information data.
helpviewer_keywords: ["IOCTL_DISK_SET_DRIVE_LAYOUT","IOCTL_DISK_SET_DRIVE_LAYOUT control","IOCTL_DISK_SET_DRIVE_LAYOUT control code [Files]","_win32_ioctl_disk_set_drive_layout","base.ioctl_disk_set_drive_layout","fs.ioctl_disk_set_drive_layout","winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT"]
old-location: fs\ioctl_disk_set_drive_layout.htm
tech.root: fs
ms.assetid: 8cace6a5-666a-4d35-a557-6bf0564dbe58
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_SET_DRIVE_LAYOUT, IOCTL_DISK_SET_DRIVE_LAYOUT control, IOCTL_DISK_SET_DRIVE_LAYOUT control code [Files], _win32_ioctl_disk_set_drive_layout, base.ioctl_disk_set_drive_layout, fs.ioctl_disk_set_drive_layout, winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT
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
 - IOCTL_DISK_SET_DRIVE_LAYOUT
 - winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT
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
 - IOCTL_DISK_SET_DRIVE_LAYOUT
---

# IOCTL_DISK_SET_DRIVE_LAYOUT IOCTL


## -description

Partitions a disk as specified by drive layout and partition information data.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the parameters specified below.

> [!NOTE]
> **IOCTL_DISK_SET_DRIVE_LAYOUT** has been superseded by [**IOCTL_DISK_SET_DRIVE_LAYOUT_EX**](ni-winioctl-ioctl_disk_set_drive_layout_ex.md), which retrieves layout information for AT and EFI (Extensible Firmware Interface) partitions.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters. You must have write access to the drive in order to use this control code.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_DISK_SET_DRIVE_LAYOUT,  // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  NULL,                         // lpOutBuffer
  0,                            // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```

## -parameters

### -param hDevice [in]

A handle to the disk.

To retrieve a device handle, call the [**CreateFile**](../fileapi/nf-fileapi-createfilew.md) function.

### -param dwIoControlCode [in]

The control code for the operation.

Use **IOCTL_DISK_SET_DRIVE_LAYOUT** for this operation.

### -param lpInBuffer [in, optional]

A pointer to the input buffer that contains the [**DRIVE_LAYOUT_INFORMATION**](ns-winioctl-drive_layout_information.md) data to be set.

### -param nInBufferSize [in]

The size of the input buffer, in bytes. It must be >= **sizeof**(DRIVE_LAYOUT_INFORMATION).

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

If the partition is on a disk formatted as type master boot record (MBR), partition size totals cannot exceed 2 TB per MBR disk. For example, a disk of type MBR can have a single 2-TB partition, two 1-TB partitions, or any combination that does not total more than 2 TB. If more space is required, a disk formatted as type GUID partition table (GPT) should be used. If third-party partitioning tools are used  to work around this limitation on disks of type MBR larger than 2 TB, configuration operations via the disk partitioning IOCTL control codes will be limited.

## -see-also

* [DRIVE_LAYOUT_INFORMATION](ns-winioctl-drive_layout_information.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/win32/FileIO/disk-management-control-codes)
* [IOCTL_DISK_SET_DRIVE_LAYOUT_EX](ni-winioctl-ioctl_disk_set_drive_layout_ex.md)
* [IOCTL_DISK_GET_DRIVE_LAYOUT](ni-winioctl-ioctl_disk_get_drive_layout.md)

