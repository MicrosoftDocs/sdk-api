---
UID: NI:winioctl.IOCTL_DISK_SET_PARTITION_INFO
title: IOCTL_DISK_SET_PARTITION_INFO
description: Sets partition information for the specified disk partition.
helpviewer_keywords: ["IOCTL_DISK_SET_PARTITION_INFO","IOCTL_DISK_SET_PARTITION_INFO control","IOCTL_DISK_SET_PARTITION_INFO control code [Files]","_win32_ioctl_disk_set_partition_info","base.ioctl_disk_set_partition_info","fs.ioctl_disk_set_partition_info","winioctl/IOCTL_DISK_SET_PARTITION_INFO"]
old-location: fs\ioctl_disk_set_partition_info.htm
tech.root: fs
ms.assetid: 868cad92-fa88-4a5a-98bb-92e73c115a22
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_SET_PARTITION_INFO, IOCTL_DISK_SET_PARTITION_INFO control, IOCTL_DISK_SET_PARTITION_INFO control code [Files], _win32_ioctl_disk_set_partition_info, base.ioctl_disk_set_partition_info, fs.ioctl_disk_set_partition_info, winioctl/IOCTL_DISK_SET_PARTITION_INFO
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
 - IOCTL_DISK_SET_PARTITION_INFO
 - winioctl/IOCTL_DISK_SET_PARTITION_INFO
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
 - IOCTL_DISK_SET_PARTITION_INFO
---

# IOCTL_DISK_SET_PARTITION_INFO IOCTL


## -description

> [!NOTE]
> **IOCTL_DISK_SET_PARTITION_INFO** has been superseded by [**IOCTL_DISK_SET_PARTITION_INFO_EX**](ni-winioctl-ioctl_disk_set_partition_info_ex.md), which retrieves layout information for AT and EFI (Extensible Firmware Interface) partitions.

Sets partition information for the specified disk partition.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_SET_PARTITION_INFO,    // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer 
  (DWORD) nInBufferSize,            // size of input buffer 
  NULL,                             // lpOutBuffer
  0,                                // nOutBufferSize
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

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of [IOCTL_DISK_SET_DRIVE_LAYOUT](ni-winioctl-ioctl_disk_set_drive_layout.md).

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [IOCTL_DISK_GET_PARTITION_INFO](ni-winioctl-ioctl_disk_get_partition_info.md)
* [IOCTL_DISK_SET_PARTITION_INFO_EX](ni-winioctl-ioctl_disk_set_partition_info_ex.md)
* [SET_PARTITION_INFORMATION](ns-winioctl-set_partition_information.md)