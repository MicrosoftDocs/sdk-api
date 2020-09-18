---
UID: NI:winioctl.FSCTL_SET_ZERO_DATA
title: FSCTL_SET_ZERO_DATA
description: Fills a specified range of a file with zeros (0).
helpviewer_keywords: ["FSCTL_SET_ZERO_DATA","FSCTL_SET_ZERO_DATA control","FSCTL_SET_ZERO_DATA control code [Files]","_win32_fsctl_set_zero_data","base.fsctl_set_zero_data","fs.fsctl_set_zero_data","winioctl/FSCTL_SET_ZERO_DATA"]
old-location: fs\fsctl_set_zero_data.htm
tech.root: fs
ms.assetid: ee32f836-682e-4c26-b7d6-82e3b7b234f9
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_ZERO_DATA, FSCTL_SET_ZERO_DATA control, FSCTL_SET_ZERO_DATA control code [Files], _win32_fsctl_set_zero_data, base.fsctl_set_zero_data, fs.fsctl_set_zero_data, winioctl/FSCTL_SET_ZERO_DATA
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
 - FSCTL_SET_ZERO_DATA
 - winioctl/FSCTL_SET_ZERO_DATA
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
 - FSCTL_SET_ZERO_DATA
---

# FSCTL_SET_ZERO_DATA IOCTL


## -description

Fills a specified range of a file with zeros (0). If the file is sparse or compressed, the NTFS file system may deallocate disk space in the file. This sets the range of bytes to zeros (0) without extending the file size.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to a file
  FSCTL_SET_ZERO_DATA,              // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
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

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

If you use the [WriteFile](../fileapi/nf-fileapi-writefile.md) function to write zeros (0) to a sparse file, the file system allocates disk space for the data that you are writing. If you use the **FSCTL_SET_ZERO_DATA** control code to write zeros (0) to a sparse file and the zero (0)  region is large enough, the file system may not allocate disk space.

If you use the **FSCTL_SET_ZERO_DATA** control code to write zeros (0) to a non-sparse file, zeros (0) are written to the file. The system allocates disk storage for all of the zero (0) range, which is equivalent to using the [WriteFile](../fileapi/nf-fileapi-writefile.md) function to write zeros (0) to a file.

The time stamps may not be updated correctly for a remote file. To ensure consistent results, use unbuffered I/O.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | Yes
SMB 3.0 with Scale-out File Shares (SO) | Yes
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | Yes

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_ZERO_DATA_INFORMATION](ns-winioctl-file_zero_data_information.md)
* [FSCTL_QUERY_ALLOCATED_RANGES](ni-winioctl-fsctl_query_allocated_ranges.md)
* [FSCTL_SET_SPARSE](ni-winioctl-fsctl_set_sparse.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)
* [Sparse Files](/windows/desktop/FileIO/sparse-files)