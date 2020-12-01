---
UID: NI:winioctl.IOCTL_VOLUME_ONLINE
title: IOCTL_VOLUME_ONLINE
description: Brings a volume online.
helpviewer_keywords: ["IOCTL_VOLUME_ONLINE","IOCTL_VOLUME_ONLINE control","IOCTL_VOLUME_ONLINE control code [Files]","fs.ioctl_volume_online","winioctl/IOCTL_VOLUME_ONLINE"]
old-location: fs\ioctl_volume_online.htm
tech.root: fs
ms.assetid: fa857959-c10e-4c64-8249-4bbf44e15eb9
ms.date: 12/05/2018
ms.keywords: IOCTL_VOLUME_ONLINE, IOCTL_VOLUME_ONLINE control, IOCTL_VOLUME_ONLINE control code [Files], fs.ioctl_volume_online, winioctl/IOCTL_VOLUME_ONLINE
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
 - IOCTL_VOLUME_ONLINE
 - winioctl/IOCTL_VOLUME_ONLINE
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
 - IOCTL_VOLUME_ONLINE
---

# IOCTL_VOLUME_ONLINE IOCTL


## -description

Brings a volume online.

**Windows Server 2003 and Windows XP:**  This control code is not supported for dynamic disks.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_VOLUME_ONLINE,          // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
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

When a volume is offline, all read, write, and IOCTL requests fail with **ERROR_NOT_READY**. You cannot take the system or boot volume offline.

When a volume is online, all requests sent to the volume are honored.

When a volume that is online is dismounted, the next call to open the volume causes it to be mounted. Taking the volume offline prevents the dismounted volume from being mounted again.

To take a volume offline, use the [IOCTL_VOLUME_OFFLINE](ni-winioctl-ioctl_volume_offline.md) control code.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | No

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [IOCTL_VOLUME_OFFLINE](ni-winioctl-ioctl_volume_offline.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)