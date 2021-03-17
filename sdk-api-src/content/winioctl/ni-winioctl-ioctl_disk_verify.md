---
UID: NI:winioctl.IOCTL_DISK_VERIFY
title: IOCTL_DISK_VERIFY
description: Verifies the specified extent on a fixed disk.
helpviewer_keywords: ["IOCTL_DISK_VERIFY","IOCTL_DISK_VERIFY control","IOCTL_DISK_VERIFY control code [Files]","_win32_ioctl_disk_verify","base.ioctl_disk_verify","fs.ioctl_disk_verify","winioctl/IOCTL_DISK_VERIFY"]
old-location: fs\ioctl_disk_verify.htm
tech.root: fs
ms.assetid: 156b217d-6cdc-4802-b711-8845934e277b
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_VERIFY, IOCTL_DISK_VERIFY control, IOCTL_DISK_VERIFY control code [Files], _win32_ioctl_disk_verify, base.ioctl_disk_verify, fs.ioctl_disk_verify, winioctl/IOCTL_DISK_VERIFY
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
 - IOCTL_DISK_VERIFY
 - winioctl/IOCTL_DISK_VERIFY
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
 - IOCTL_DISK_VERIFY
---

# IOCTL_DISK_VERIFY IOCTL


## -description

Verifies the specified extent on a fixed disk.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_DISK_VERIFY,            // dwIoControlCode
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

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [VERIFY_INFORMATION](ns-winioctl-verify_information.md)