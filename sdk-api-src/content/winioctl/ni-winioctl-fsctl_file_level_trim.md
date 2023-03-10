---
UID: NI:winioctl.FSCTL_FILE_LEVEL_TRIM
title: FSCTL_FILE_LEVEL_TRIM
description: Indicates ranges within the specified file that do not need to be stored by the storage system.
helpviewer_keywords: ["FSCTL_FILE_LEVEL_TRIM","FSCTL_FILE_LEVEL_TRIM control","FSCTL_FILE_LEVEL_TRIM control code [Files]","fs.fsctl_file_level_trim","winioctl/FSCTL_FILE_LEVEL_TRIM"]
old-location: fs\fsctl_file_level_trim.htm
tech.root: fs
ms.assetid: 2d466a98-f7b2-4638-942c-1cf9016d0bf9
ms.date: 12/05/2018
ms.keywords: FSCTL_FILE_LEVEL_TRIM, FSCTL_FILE_LEVEL_TRIM control, FSCTL_FILE_LEVEL_TRIM control code [Files], fs.fsctl_file_level_trim, winioctl/FSCTL_FILE_LEVEL_TRIM
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - FSCTL_FILE_LEVEL_TRIM
 - winioctl/FSCTL_FILE_LEVEL_TRIM
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
 - FSCTL_FILE_LEVEL_TRIM
---

# FSCTL_FILE_LEVEL_TRIM IOCTL


## -description

Indicates ranges within the specified file that do not need to be stored by the storage system.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // Handle to a file
  FSCTL_FILE_LEVEL_TRIM,            // dwIoControlCode
  (LPVOID) lpInBuffer,              // Input buffer
  (DWORD) nInBufferSize,            // Size of input buffer
  (LPVOID) lpOutBuffer,             // Output buffer
  (DWORD) nOutBufferSize,           // Size of output buffer
  (LPDWORD) lpBytesReturned,        // Number of bytes returned
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

The **FSCTL_FILE_LEVEL_TRIM** control code is a hint to the underlying storage system. When a range of bytes has been trimmed, if that range is later read again, the data returned may be the original data before the trim operation—all zeros (0x00 bytes), all ones (0xff bytes), or a combination of these. Before the trim operation is passed to the underlying storage system, the input ranges are reduced to align with page boundaries (4,096 bytes on 32-bit and x64-based editions of Windows, 8,192 bytes on Itanium-Based editions of Windows).

If an error occurs while processing the [FILE_LEVEL_TRIM_RANGE](ns-winioctl-file_level_trim_range.md) entries that follow the [FILE_LEVEL_TRIM](ns-winioctl-file_level_trim.md) structure in the input buffer pointed to by the *lpInBuffer* parameter, processing stops and the **NumRangesProcessed** member of the [FILE_LEVEL_TRIM_OUTPUT](ns-winioctl-file_level_trim_output.md) structure pointed to by the *lpOutBuffer* parameter will indicate the ranges that were successfully processed. Any ranges between **NumRangesProcessed** and the **NumRanges** member of the **FILE_LEVEL_TRIM** structure were not processed.

The **FSCTL_FILE_LEVEL_TRIM** control code is not compatible with encrypted or compressed files ([GetFileAttributes](../fileapi/nf-fileapi-getfileattributesa.md) returns **FILE_ATTRIBUTE_ENCRYPTED** or **FILE_ATTRIBUTE_COMPRESSED**) and will fail with **ERROR_INVALID_PARAMETER**. Sparse files (indicated by **FILE_ATTRIBUTE_SPARSE_FILE**) are supported, but only ranges that have been allocated can be trimmed. Files on volumes encrypted by BitLocker technology are supported, while individually encrypted files are not.

The **FSCTL_FILE_LEVEL_TRIM** control code does not participate in transactions. If a **FSCTL_FILE_LEVEL_TRIM** control code is processed during a transaction, and the transaction is aborted, the trim will not be rolled back with the transaction.

Ranges that are successfully trimmed will be removed from the filesystem cache.

Ranges that are trimmed can be beyond the valid data length (VDL) up to the end-of-file (EOF).

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | Yes
SMB 3.0 with Scale-out File Shares (SO) | Yes
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | No

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_LEVEL_TRIM](ns-winioctl-file_level_trim.md)
* [FILE_LEVEL_TRIM_OUTPUT](ns-winioctl-file_level_trim_output.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)