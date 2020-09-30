---
UID: NI:winioctl.IOCTL_DISK_GET_LENGTH_INFO
title: IOCTL_DISK_GET_LENGTH_INFO
description: Retrieves the length of the specified disk, volume, or partition.
helpviewer_keywords: ["IOCTL_DISK_GET_LENGTH_INFO","IOCTL_DISK_GET_LENGTH_INFO control","IOCTL_DISK_GET_LENGTH_INFO control code [Files]","_win32_ioctl_disk_get_length_info","base.ioctl_disk_get_length_info","fs.ioctl_disk_get_length_info","winioctl/IOCTL_DISK_GET_LENGTH_INFO"]
old-location: fs\ioctl_disk_get_length_info.htm
tech.root: fs
ms.assetid: 8d4bd6e3-f0f3-40d6-b0ba-75155282f64a
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_LENGTH_INFO, IOCTL_DISK_GET_LENGTH_INFO control, IOCTL_DISK_GET_LENGTH_INFO control code [Files], _win32_ioctl_disk_get_length_info, base.ioctl_disk_get_length_info, fs.ioctl_disk_get_length_info, winioctl/IOCTL_DISK_GET_LENGTH_INFO
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
 - IOCTL_DISK_GET_LENGTH_INFO
 - winioctl/IOCTL_DISK_GET_LENGTH_INFO
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
 - IOCTL_DISK_GET_LENGTH_INFO
---

# IOCTL_DISK_GET_LENGTH_INFO IOCTL


## -description

Retrieves the length of the specified disk, volume, or partition.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_DISK_GET_LENGTH_INFO,   // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
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

Volume handles do not have access to the full volume. To read or write to the last few sectors of a volume, you must call [FSCTL_ALLOW_EXTENDED_DASD_IO](ni-winioctl-fsctl_allow_extended_dasd_io.md), which instructs the file system to not perform any boundary checks.

This operation should be used instead of [IOCTL_DISK_GET_PARTITION_INFO_EX](ni-winioctl-ioctl_disk_get_partition_info_ex.md) for volumes that do not have partition info—such as partition type or number of hidden sectors.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [GET_LENGTH_INFORMATION](ns-winioctl-get_length_information.md)