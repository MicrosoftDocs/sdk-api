---
UID: NI:winioctl.FSCTL_SET_SPARSE
title: FSCTL_SET_SPARSE
description: Marks the indicated file as sparse or not sparse. In a sparse file, large ranges of zeros may not require disk allocation.
helpviewer_keywords: ["FSCTL_SET_SPARSE","FSCTL_SET_SPARSE control","FSCTL_SET_SPARSE control code [Files]","_win32_fsctl_set_sparse","base.fsctl_set_sparse","fs.fsctl_set_sparse","winioctl/FSCTL_SET_SPARSE"]
old-location: fs\fsctl_set_sparse.htm
tech.root: fs
ms.assetid: aa8f5880-f831-49b6-8359-fe07c78c032f
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_SPARSE, FSCTL_SET_SPARSE control, FSCTL_SET_SPARSE control code [Files], _win32_fsctl_set_sparse, base.fsctl_set_sparse, fs.fsctl_set_sparse, winioctl/FSCTL_SET_SPARSE
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
 - FSCTL_SET_SPARSE
 - winioctl/FSCTL_SET_SPARSE
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
 - FSCTL_SET_SPARSE
---

# FSCTL_SET_SPARSE IOCTL


## -description

Marks the indicated file as sparse or  not sparse. In a sparse file, large ranges of zeros may not require disk allocation. Space for nonzero data will be allocated as needed as the file is written.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                         // handle to a file
  FSCTL_SET_SPARSE,                         // dwIoControlCode
  (PFILE_SET_SPARSE_BUFFER) lpInBuffer,     // input buffer
  (DWORD) nInBufferSize,                    // size of input buffer
  NULL,                                     // lpOutBuffer
  0,                                        // nOutBufferSize
  (LPDWORD) lpBytesReturned,                // number of bytes returned
  (LPOVERLAPPED) lpOverlapped               // OVERLAPPED structure
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

For the implications of overlapped I/O on this operation, see the Remarks section of [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md).

The **FSCTL_SET_SPARSE** control code sets or clears the **FILE_ATTRIBUTE_SPARSE_FILE** attribute of the specified file.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:**  A clear operation is valid only on files that no longer have any sparse regions. Performing a clear operation on a file with sparse regions can have unpredictable results. You can determine whether there are any sparse regions in a file by using the [FSCTL_QUERY_ALLOCATED_RANGES](ni-winioctl-fsctl_query_allocated_ranges.md) control code.

If the *lpInBuffer* parameter is **NULL**, the operation will behave the same as if the **SetSparse** member of the [FILE_SET_SPARSE_BUFFER](ns-winioctl-file_set_sparse_buffer.md) structure were **TRUE**. In other words, the operation sets the file to a sparse file.

**Windows Server 2003 and Windows XP:**  If a [FILE_SET_SPARSE_BUFFER](ns-winioctl-file_set_sparse_buffer.md) structure is passed in the *lpInBuffer* parameter, the only valid value for the **SetSparse** member is **TRUE**, which sets the file to a sparse file. Passing **FALSE** in the **FILE_SET_SPARSE_BUFFER** structure will cause this function call to fail. The only way to clear this attribute is to overwrite the file (for example, by calling the [CreateFile](../fileapi/nf-fileapi-createfilea.md) function with the **CREATE_ALWAYS** flag).

You cannot create a sparse file by calling [CreateFile](../fileapi/nf-fileapi-createfilea.md) with **FILE_ATTRIBUTE_SPARSE_FILE** in the *dwFlagsAndAttributes* parameter. You must use the **FSCTL_SET_SPARSE** control code.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use unbuffered I/O.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | Yes
SMB 3.0 with Scale-out File Shares (SO) | Yes
Cluster Shared Volume File System (CsvFS) | See Comment
Resilient File System (ReFS) | Yes

CsvFs will do redirected IO for sparse files. CsvFs allows making file sparse only when the file is opened exclusively by a node. SMB 3.0 Transparent Failover does not support buffered write.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_SET_SPARSE_BUFFER](ns-winioctl-file_set_sparse_buffer.md)
* [FSCTL_QUERY_ALLOCATED_RANGES](ni-winioctl-fsctl_query_allocated_ranges.md)
* [FSCTL_SET_ZERO_DATA](ni-winioctl-fsctl_set_zero_data.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)
* [Sparse Files](/windows/desktop/FileIO/sparse-files)