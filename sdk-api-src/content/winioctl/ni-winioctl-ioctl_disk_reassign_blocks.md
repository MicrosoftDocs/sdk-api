---
UID: NI:winioctl.IOCTL_DISK_REASSIGN_BLOCKS
title: IOCTL_DISK_REASSIGN_BLOCKS
description: Directs the disk device to map one or more blocks to its spare-block pool. (IOCTL_DISK_REASSIGN_BLOCKS)
helpviewer_keywords: ["IOCTL_DISK_REASSIGN_BLOCKS","IOCTL_DISK_REASSIGN_BLOCKS control","IOCTL_DISK_REASSIGN_BLOCKS control code [Files]","_win32_ioctl_disk_reassign_blocks","base.ioctl_disk_reassign_blocks","fs.ioctl_disk_reassign_blocks","winioctl/IOCTL_DISK_REASSIGN_BLOCKS"]
old-location: fs\ioctl_disk_reassign_blocks.htm
tech.root: fs
ms.assetid: 57343bc9-9dd4-47a3-8130-07ea330eb4d3
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_REASSIGN_BLOCKS, IOCTL_DISK_REASSIGN_BLOCKS control, IOCTL_DISK_REASSIGN_BLOCKS control code [Files], _win32_ioctl_disk_reassign_blocks, base.ioctl_disk_reassign_blocks, fs.ioctl_disk_reassign_blocks, winioctl/IOCTL_DISK_REASSIGN_BLOCKS
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
 - IOCTL_DISK_REASSIGN_BLOCKS
 - winioctl/IOCTL_DISK_REASSIGN_BLOCKS
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
 - IOCTL_DISK_REASSIGN_BLOCKS
---

# IOCTL_DISK_REASSIGN_BLOCKS IOCTL


## -description

Directs the disk device to map one or more blocks to its spare-block pool.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_DISK_REASSIGN_BLOCKS,   // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer 
  (DWORD) nInBufferSize,        // size of input buffer 
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

The [REASSIGN_BLOCKS](ns-winioctl-reassign_blocks.md) structure that the **IOCTL_DISK_REASSIGN_BLOCKS** control code uses only supports drives where the Logical Block Address (LBA) fits into a 4-byte value (typically up to 2 TB). For larger drives the [REASSIGN_BLOCKS_EX](ns-winioctl-reassign_blocks_ex.md) structure that the [IOCTL_DISK_REASSIGN_BLOCKS_EX](ni-winioctl-ioctl_disk_reassign_blocks_ex.md) control code uses supports 8-byte LBAs. For compatibility, the **IOCTL_DISK_REASSIGN_BLOCKS** control code and **REASSIGN_BLOCKS** structure should be used where possible.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [IOCTL_DISK_REASSIGN_BLOCKS_EX](ni-winioctl-ioctl_disk_reassign_blocks_ex.md)
* [REASSIGN_BLOCKS](ns-winioctl-reassign_blocks.md)
* [REASSIGN_BLOCKS_EX](ns-winioctl-reassign_blocks_ex.md)
