---
UID: NI:winioctl.IOCTL_DISK_REASSIGN_BLOCKS_EX
title: IOCTL_DISK_REASSIGN_BLOCKS_EX
description: Directs the disk device to map one or more blocks to its spare-block pool. (IOCTL_DISK_REASSIGN_BLOCKS_EX)
helpviewer_keywords: ["IOCTL_DISK_REASSIGN_BLOCKS_EX","IOCTL_DISK_REASSIGN_BLOCKS_EX control","IOCTL_DISK_REASSIGN_BLOCKS_EX control code [Files]","base.ioctl_disk_reassign_blocks_ex","fs.ioctl_disk_reassign_blocks_ex","winioctl/IOCTL_DISK_REASSIGN_BLOCKS_EX"]
old-location: fs\ioctl_disk_reassign_blocks_ex.htm
tech.root: fs
ms.assetid: 126ffefa-165b-4ca1-a905-1aebc8e790c7
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_REASSIGN_BLOCKS_EX, IOCTL_DISK_REASSIGN_BLOCKS_EX control, IOCTL_DISK_REASSIGN_BLOCKS_EX control code [Files], base.ioctl_disk_reassign_blocks_ex, fs.ioctl_disk_reassign_blocks_ex, winioctl/IOCTL_DISK_REASSIGN_BLOCKS_EX
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IOCTL_DISK_REASSIGN_BLOCKS_EX
 - winioctl/IOCTL_DISK_REASSIGN_BLOCKS_EX
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
 - IOCTL_DISK_REASSIGN_BLOCKS_EX
---

# IOCTL_DISK_REASSIGN_BLOCKS_EX IOCTL


## -description

Directs the disk device to map one or more blocks to its spare-block pool.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_REASSIGN_BLOCKS_EX,    // dwIoControlCode
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

The [REASSIGN_BLOCKS_EX](ns-winioctl-reassign_blocks_ex.md) structure that the **IOCTL_DISK_REASSIGN_BLOCKS_EX** control code uses supports 8-byte Logical Block Addresses (LBA). For compatibility, the [IOCTL_DISK_REASSIGN_BLOCKS](ni-winioctl-ioctl_disk_reassign_blocks.md) control code and [REASSIGN_BLOCKS](ns-winioctl-reassign_blocks.md) structure should be used where the LBA fits in the 4-byte LBA that the **REASSIGN_BLOCKS** structure supports (typically drives up to 2 TB).

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [IOCTL_DISK_REASSIGN_BLOCKS](ni-winioctl-ioctl_disk_reassign_blocks.md)
* [REASSIGN_BLOCKS](ns-winioctl-reassign_blocks.md)
* [REASSIGN_BLOCKS_EX](ns-winioctl-reassign_blocks_ex.md)
