---
UID: NI:winioctl.FSCTL_QUERY_ON_DISK_VOLUME_INFO
title: FSCTL_QUERY_ON_DISK_VOLUME_INFO
description: Requests UDF-specific volume information.
helpviewer_keywords: ["FSCTL_QUERY_ON_DISK_VOLUME_INFO","FSCTL_QUERY_ON_DISK_VOLUME_INFO control","FSCTL_QUERY_ON_DISK_VOLUME_INFO control code [Files]","fs.fsctl_query_on_disk_volume_info","winioctl/FSCTL_QUERY_ON_DISK_VOLUME_INFO"]
old-location: fs\fsctl_query_on_disk_volume_info.htm
tech.root: fs
ms.assetid: 6d34007e-4e6f-433e-9d85-9b2743e1c1d2
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_ON_DISK_VOLUME_INFO, FSCTL_QUERY_ON_DISK_VOLUME_INFO control, FSCTL_QUERY_ON_DISK_VOLUME_INFO control code [Files], fs.fsctl_query_on_disk_volume_info, winioctl/FSCTL_QUERY_ON_DISK_VOLUME_INFO
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FSCTL_QUERY_ON_DISK_VOLUME_INFO
 - winioctl/FSCTL_QUERY_ON_DISK_VOLUME_INFO
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
 - FSCTL_QUERY_ON_DISK_VOLUME_INFO
---

# FSCTL_QUERY_ON_DISK_VOLUME_INFO IOCTL


## -description

Requests UDF-specific volume information.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_QUERY_ON_DISK_VOLUME_INFO,  // dwIoControlCode
  NULL,                             // input buffer
  0,                                // size of input buffer
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

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | Yes
SMB 3.0 with Scale-out File Shares (SO) | Yes
Cluster Shared Volume File System (CsvFS) | No
Resilient File System (ReFS) | No

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_QUERY_ON_DISK_VOL_INFO_BUFFER](ns-winioctl-file_query_on_disk_vol_info_buffer.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)