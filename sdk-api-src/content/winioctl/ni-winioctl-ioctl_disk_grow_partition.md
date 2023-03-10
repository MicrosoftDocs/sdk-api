---
UID: NI:winioctl.IOCTL_DISK_GROW_PARTITION
title: IOCTL_DISK_GROW_PARTITION
description: Enlarges the specified partition.
helpviewer_keywords: ["IOCTL_DISK_GROW_PARTITION","IOCTL_DISK_GROW_PARTITION control","IOCTL_DISK_GROW_PARTITION control code [Files]","base.ioctl_disk_grow_partition","fs.ioctl_disk_grow_partition","winioctl/IOCTL_DISK_GROW_PARTITION"]
old-location: fs\ioctl_disk_grow_partition.htm
tech.root: fs
ms.assetid: bbcb0bee-a507-4abb-83df-328f3aa6caaa
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GROW_PARTITION, IOCTL_DISK_GROW_PARTITION control, IOCTL_DISK_GROW_PARTITION control code [Files], base.ioctl_disk_grow_partition, fs.ioctl_disk_grow_partition, winioctl/IOCTL_DISK_GROW_PARTITION
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
 - IOCTL_DISK_GROW_PARTITION
 - winioctl/IOCTL_DISK_GROW_PARTITION
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
 - IOCTL_DISK_GROW_PARTITION
---

# IOCTL_DISK_GROW_PARTITION IOCTL


## -description

Enlarges the specified partition.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_DISK_GROW_PARTITION,    // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of the input buffer
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

You can extend or shrink a live partition, and the partition can be open for sharing during the extend or shrink operation. 

You do not need to lock a partition that you are extending, nor do you need to shut down other applications or services during the extend operation.

For more information, see [DISK_GROW_PARTITION](ns-winioctl-disk_grow_partition.md).

## -see-also

* [DISK_GROW_PARTITION](ns-winioctl-disk_grow_partition.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)