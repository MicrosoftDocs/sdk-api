---
UID: NI:winioctl.FSCTL_GET_NTFS_VOLUME_DATA
title: FSCTL_GET_NTFS_VOLUME_DATA
description: Retrieves information about the specified NTFS file system volume.
helpviewer_keywords: ["FSCTL_GET_NTFS_VOLUME_DATA","FSCTL_GET_NTFS_VOLUME_DATA control","FSCTL_GET_NTFS_VOLUME_DATA control code [Files]","_win32_fsctl_get_ntfs_volume_data","base.fsctl_get_ntfs_volume_data","fs.fsctl_get_ntfs_volume_data","winioctl/FSCTL_GET_NTFS_VOLUME_DATA"]
old-location: fs\fsctl_get_ntfs_volume_data.htm
tech.root: fs
ms.assetid: b5690b4f-3967-41d8-bf11-70f8b1da79ad
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_NTFS_VOLUME_DATA, FSCTL_GET_NTFS_VOLUME_DATA control, FSCTL_GET_NTFS_VOLUME_DATA control code [Files], _win32_fsctl_get_ntfs_volume_data, base.fsctl_get_ntfs_volume_data, fs.fsctl_get_ntfs_volume_data, winioctl/FSCTL_GET_NTFS_VOLUME_DATA
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
 - FSCTL_GET_NTFS_VOLUME_DATA
 - winioctl/FSCTL_GET_NTFS_VOLUME_DATA
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
 - FSCTL_GET_NTFS_VOLUME_DATA
---

# FSCTL_GET_NTFS_VOLUME_DATA IOCTL


## -description

Retrieves information about the specified NTFS file system volume.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_GET_NTFS_VOLUME_DATA,   // dwIoControlCode
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

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [NTFS_VOLUME_DATA_BUFFER](ns-winioctl-ntfs_volume_data_buffer.md)
* [NTFS_EXTENDED_VOLUME_DATA](ns-winioctl-ntfs_extended_volume_data.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)
