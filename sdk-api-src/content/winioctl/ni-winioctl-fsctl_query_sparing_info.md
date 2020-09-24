---
UID: NI:winioctl.FSCTL_QUERY_SPARING_INFO
title: FSCTL_QUERY_SPARING_INFO
description: Retrieves the defect management properties of the volume. Used for UDF file systems.
helpviewer_keywords: ["FSCTL_QUERY_SPARING_INFO","FSCTL_QUERY_SPARING_INFO control","FSCTL_QUERY_SPARING_INFO control code [Files]","fs.fsctl_query_sparing_info","winioctl/FSCTL_QUERY_SPARING_INFO"]
old-location: fs\fsctl_query_sparing_info.htm
tech.root: fs
ms.assetid: 72122388-a42f-4c67-9539-20eb4c59dcf0
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_SPARING_INFO, FSCTL_QUERY_SPARING_INFO control, FSCTL_QUERY_SPARING_INFO control code [Files], fs.fsctl_query_sparing_info, winioctl/FSCTL_QUERY_SPARING_INFO
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
 - FSCTL_QUERY_SPARING_INFO
 - winioctl/FSCTL_QUERY_SPARING_INFO
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
 - FSCTL_QUERY_SPARING_INFO
---

# FSCTL_QUERY_SPARING_INFO IOCTL


## -description

Retrieves the defect management properties of the volume. Used for UDF file systems.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_QUERY_SPARING_INFO,     // dwIoControlCode
  NULL,                         // input buffer
  0,                            // size of input buffer
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

One scenario this control code can be used for is by an application that reports volume statistics to the user and warns if the volume is running out of free storage space.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | Yes
SMB 3.0 with Scale-out File Shares (SO) | Yes
Cluster Shared Volume File System (CsvFS) | No
Resilient File System (ReFS) | Yes

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_QUERY_SPARING_BUFFER](ns-winioctl-file_query_sparing_buffer.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)