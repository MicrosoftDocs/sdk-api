---
UID: NI:winioctl.FSCTL_FILESYSTEM_GET_STATISTICS
title: FSCTL_FILESYSTEM_GET_STATISTICS
description: Retrieves the information from various file system performance counters.
helpviewer_keywords: ["FSCTL_FILESYSTEM_GET_STATISTICS","FSCTL_FILESYSTEM_GET_STATISTICS control","FSCTL_FILESYSTEM_GET_STATISTICS control code [Files]","base.fsctl_filesystem_get_statistics","fs.fsctl_filesystem_get_statistics","winioctl/FSCTL_FILESYSTEM_GET_STATISTICS"]
old-location: fs\fsctl_filesystem_get_statistics.htm
tech.root: fs
ms.assetid: d975d32c-1290-4397-8c05-6c515af4c450
ms.date: 12/05/2018
ms.keywords: FSCTL_FILESYSTEM_GET_STATISTICS, FSCTL_FILESYSTEM_GET_STATISTICS control, FSCTL_FILESYSTEM_GET_STATISTICS control code [Files], base.fsctl_filesystem_get_statistics, fs.fsctl_filesystem_get_statistics, winioctl/FSCTL_FILESYSTEM_GET_STATISTICS
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
 - FSCTL_FILESYSTEM_GET_STATISTICS
 - winioctl/FSCTL_FILESYSTEM_GET_STATISTICS
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
 - FSCTL_FILESYSTEM_GET_STATISTICS
---

# FSCTL_FILESYSTEM_GET_STATISTICS IOCTL


## -description

Retrieves the information from various file system performance counters.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_FILESYSTEM_GET_STATISTICS,  // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
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
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | Yes

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILESYSTEM_STATISTICS](ns-winioctl-filesystem_statistics.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)