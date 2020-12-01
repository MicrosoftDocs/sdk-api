---
UID: NI:winioctl.FSCTL_FILESYSTEM_GET_STATISTICS_EX
title: FSCTL_FILESYSTEM_GET_STATISTICS_EX
description: Retrieves the information from various file system performance counters.Support for this control code started with Windows 10.
helpviewer_keywords: ["FSCTL_FILESYSTEM_GET_STATISTICS_EX","FSCTL_FILESYSTEM_GET_STATISTICS_EX control","FSCTL_FILESYSTEM_GET_STATISTICS_EX control code [Files]","fs.fsctl_filesystem_get_statistics_ex","winioctl/FSCTL_FILESYSTEM_GET_STATISTICS_EX"]
old-location: fs\fsctl_filesystem_get_statistics_ex.htm
tech.root: fs
ms.assetid: 9B2C1F94-BA25-4534-BBD8-8D1EC5D05AF1
ms.date: 12/05/2018
ms.keywords: FSCTL_FILESYSTEM_GET_STATISTICS_EX, FSCTL_FILESYSTEM_GET_STATISTICS_EX control, FSCTL_FILESYSTEM_GET_STATISTICS_EX control code [Files], fs.fsctl_filesystem_get_statistics_ex, winioctl/FSCTL_FILESYSTEM_GET_STATISTICS_EX
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - FSCTL_FILESYSTEM_GET_STATISTICS_EX
 - winioctl/FSCTL_FILESYSTEM_GET_STATISTICS_EX
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
 - FSCTL_FILESYSTEM_GET_STATISTICS_EX
---

# FSCTL_FILESYSTEM_GET_STATISTICS_EX IOCTL


## -description

Retrieves the information from various file system performance counters.Support for this control code started with Windows 10.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                     // handle to device
  FSCTL_FILESYSTEM_GET_STATISTICS_EX,   // dwIoControlCode
  NULL,                                 // lpInBuffer
  0,                                    // nInBufferSize
  (LPVOID) lpOutBuffer,                 // output buffer
  (DWORD) nOutBufferSize,               // size of output buffer
  (LPDWORD) lpBytesReturned,            // number of bytes returned
  (LPOVERLAPPED) lpOverlapped           // OVERLAPPED structure
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

In Windows 10, this code is supported by the following technologies.

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
* [FILESYSTEM_STATISTICS_EX](ns-winioctl-filesystem_statistics_ex.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)