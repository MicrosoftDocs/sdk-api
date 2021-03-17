---
UID: NI:winioctl.IOCTL_VOLUME_OFFLINE
title: IOCTL_VOLUME_OFFLINE
description: Takes a volume offline.
helpviewer_keywords: ["IOCTL_VOLUME_OFFLINE","IOCTL_VOLUME_OFFLINE control","IOCTL_VOLUME_OFFLINE control code [Files]","fs.ioctl_volume_offline","winioctl/IOCTL_VOLUME_OFFLINE"]
old-location: fs\ioctl_volume_offline.htm
tech.root: fs
ms.assetid: 7c9b97eb-c167-41cd-b235-7a9d7830915e
ms.date: 12/05/2018
ms.keywords: IOCTL_VOLUME_OFFLINE, IOCTL_VOLUME_OFFLINE control, IOCTL_VOLUME_OFFLINE control code [Files], fs.ioctl_volume_offline, winioctl/IOCTL_VOLUME_OFFLINE
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
 - IOCTL_VOLUME_OFFLINE
 - winioctl/IOCTL_VOLUME_OFFLINE
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
 - IOCTL_VOLUME_OFFLINE
---

# IOCTL_VOLUME_OFFLINE IOCTL


## -description

Takes a volume offline.

**Windows Server 2003 and Windows XP:**  This control code is not supported for dynamic disks.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_VOLUME_OFFLINE,         // dwIoControlCode
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

Applications must first successfully dismount the file system - via [FSCTL_DISMOUNT_VOLUME](ni-winioctl-fsctl_dismount_volume.md) - before using **IOCTL_VOLUME_OFFLINE**.

When a volume that is online is dismounted, the next call to open the volume causes it to be mounted.  Taking the volume offline using the same volume handle as was used for the dismount prevents the dismounted volume from being mounted again.

When a volume is online, all requests sent to the volume are honored.

When a volume that is online is dismounted, the next call to open the volume causes it to be mounted. Taking the volume offline prevents the dismounted volume from being mounted again.

To bring a volume online, use the [IOCTL_VOLUME_ONLINE](ni-winioctl-ioctl_volume_online.md) control code.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | No

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [IOCTL_VOLUME_ONLINE](ni-winioctl-ioctl_volume_online.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)