---
UID: NI:winioctl.FSCTL_GET_REPARSE_POINT
title: FSCTL_GET_REPARSE_POINT
description: Retrieves the reparse point data associated with the file or directory identified by the specified handle.
helpviewer_keywords: ["FSCTL_GET_REPARSE_POINT","FSCTL_GET_REPARSE_POINT control","FSCTL_GET_REPARSE_POINT control code [Files]","_win32_fsctl_get_reparse_point","base.fsctl_get_reparse_point","fs.fsctl_get_reparse_point","winioctl/FSCTL_GET_REPARSE_POINT"]
old-location: fs\fsctl_get_reparse_point.htm
tech.root: fs
ms.assetid: 6f1b7ea2-aed6-4ab4-8e92-1b77ab5cfefb
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_REPARSE_POINT, FSCTL_GET_REPARSE_POINT control, FSCTL_GET_REPARSE_POINT control code [Files], _win32_fsctl_get_reparse_point, base.fsctl_get_reparse_point, fs.fsctl_get_reparse_point, winioctl/FSCTL_GET_REPARSE_POINT
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
 - FSCTL_GET_REPARSE_POINT
 - winioctl/FSCTL_GET_REPARSE_POINT
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
 - FSCTL_GET_REPARSE_POINT
---

# FSCTL_GET_REPARSE_POINT IOCTL


## -description

Retrieves the reparse point data associated with the file or directory identified by the specified handle.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to file or directory
  FSCTL_GET_REPARSE_POINT,      // dwIoControlCode
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

Otherwise, Status is set to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

For the implications of overlapped I/O on this operation, see the Remarks section of 
[DeviceIoControl](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol).

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | Yes
SMB 3.0 with Scale-out File Shares (SO) | Yes
Cluster Shared Volume File System (CsvFS) | No
Resilient File System (ReFS) | Yes

CsvFs does not support reparse points.

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_DELETE_REPARSE_POINT](ni-winioctl-fsctl_delete_reparse_point.md)
* [FSCTL_SET_REPARSE_POINT](ni-winioctl-fsctl_set_reparse_point.md)
* [REPARSE_GUID_DATA_BUFFER](../winnt/ns-winnt-reparse_guid_data_buffer.md)
* [Reparse Points](/windows/desktop/FileIO/reparse-points)