---
UID: NI:winioctl.IOCTL_DISK_RESET_SNAPSHOT_INFO
title: IOCTL_DISK_RESET_SNAPSHOT_INFO
description: Clears all Volume Shadow Copy Service (VSS) hardware-based shadow copy (also called &quot;snapshot&quot;) information from the disk.
helpviewer_keywords: ["IOCTL_DISK_RESET_SNAPSHOT_INFO","IOCTL_DISK_RESET_SNAPSHOT_INFO control","IOCTL_DISK_RESET_SNAPSHOT_INFO control code [Files]","fs.ioctl_disk_reset_snapshot_info","winioctl/IOCTL_DISK_RESET_SNAPSHOT_INFO"]
old-location: fs\ioctl_disk_reset_snapshot_info.htm
tech.root: fs
ms.assetid: 522f469e-9630-4fa3-a157-7090c58a9856
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_RESET_SNAPSHOT_INFO, IOCTL_DISK_RESET_SNAPSHOT_INFO control, IOCTL_DISK_RESET_SNAPSHOT_INFO control code [Files], fs.ioctl_disk_reset_snapshot_info, winioctl/IOCTL_DISK_RESET_SNAPSHOT_INFO
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IOCTL_DISK_RESET_SNAPSHOT_INFO
 - winioctl/IOCTL_DISK_RESET_SNAPSHOT_INFO
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
 - IOCTL_DISK_RESET_SNAPSHOT_INFO
---

# IOCTL_DISK_RESET_SNAPSHOT_INFO IOCTL


## -description

Clears all Volume Shadow Copy Service (VSS) hardware-based shadow copy (also called "snapshot") information from the disk.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_RESET_SNAPSHOT_INFO,   // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
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

The disk whose handle is used when this IOCTL is issued might be in the offline state when the IOCTL is issued. If the disk is put in the offline state by using the disk management Microsoft Management Console (MMC) snap-in, the disk will have its read-only attribute set, which will cause this IOCTL to fail. However, if the disk partition utility (Diskpart.exe) is used to put the disk in the offline state, the read-only attribute for the disk is not set. For this reason, it is best to use the disk partition utility to put a disk in the offline state.

> [!NOTE]
> One side effect of using this IOCTL is that Disk Management tools will now report an additional partition on GPT disks of the type "UNKNOWN." This 256KB partition is created by using the IOCTL and is the shadow copy partition that is used in the restore process. The partition is expected and can be ignored by system administrators.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)