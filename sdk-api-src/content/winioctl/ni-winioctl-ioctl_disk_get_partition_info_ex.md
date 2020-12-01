---
UID: NI:winioctl.IOCTL_DISK_GET_PARTITION_INFO_EX
title: IOCTL_DISK_GET_PARTITION_INFO_EX
description: Retrieves extended information about the type, size, and nature of a disk partition.
helpviewer_keywords: ["IOCTL_DISK_GET_PARTITION_INFO_EX","IOCTL_DISK_GET_PARTITION_INFO_EX control","IOCTL_DISK_GET_PARTITION_INFO_EX control code [Files]","_win32_ioctl_disk_get_partition_info_ex","base.ioctl_disk_get_partition_info_ex","fs.ioctl_disk_get_partition_info_ex","winioctl/IOCTL_DISK_GET_PARTITION_INFO_EX"]
old-location: fs\ioctl_disk_get_partition_info_ex.htm
tech.root: fs
ms.assetid: f84f8be6-2b01-4a20-8669-cb1a55c32907
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_PARTITION_INFO_EX, IOCTL_DISK_GET_PARTITION_INFO_EX control, IOCTL_DISK_GET_PARTITION_INFO_EX control code [Files], _win32_ioctl_disk_get_partition_info_ex, base.ioctl_disk_get_partition_info_ex, fs.ioctl_disk_get_partition_info_ex, winioctl/IOCTL_DISK_GET_PARTITION_INFO_EX
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
 - IOCTL_DISK_GET_PARTITION_INFO_EX
 - winioctl/IOCTL_DISK_GET_PARTITION_INFO_EX
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
 - IOCTL_DISK_GET_PARTITION_INFO_EX
---

# IOCTL_DISK_GET_PARTITION_INFO_EX IOCTL


## -description

Retrieves extended information about the type, size, and nature of a disk partition.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to a partition
  IOCTL_DISK_GET_PARTITION_INFO_EX, // dwIoControlCode
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

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

The **IOCTL_DISK_GET_PARTITION_INFO_EX** control code is supported on basic disks. It is only supported on dynamic disks that are boot or system disks, or have retained entries in the partition table. The [DiskPart.exe](/windows-server/administration/windows-commands/diskpart) command **RETAIN** can be used to do this for other dynamic simple partitions.

The disk support can be summarized as follows.

Disk type | IOCTL_DISK_GET_PARTITION_INFO | IOCTL_DISK_GET_PARTITION_INFO_EX
----------|-------------------------------|---------------------------------
Basic master boot record (MBR) | Yes | Yes
Basic GUID partition table (GPT) | No | Yes
Dynamic MBR boot/system | Yes | Yes
Dynamic MBR data | Yes | No
Dynamic GPT boot/system | No | Yes
Dynamic GPT data | No | No

Currently, GPT is supported only on 64-bit systems.

If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of [IOCTL_DISK_SET_DRIVE_LAYOUT](ni-winioctl-ioctl_disk_set_drive_layout.md).

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [File System Recognition](/windows/desktop/FileIO/file-system-recognition)
* [IOCTL_DISK_SET_PARTITION_INFO_EX](ni-winioctl-ioctl_disk_set_partition_info_ex.md)
* [PARTITION_INFORMATION_EX](ns-winioctl-partition_information_ex.md)