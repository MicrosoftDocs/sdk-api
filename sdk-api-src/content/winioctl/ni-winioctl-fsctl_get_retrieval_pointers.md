---
UID: NI:winioctl.FSCTL_GET_RETRIEVAL_POINTERS
title: FSCTL_GET_RETRIEVAL_POINTERS
description: Given a file handle, retrieves a data structure that describes the allocation and location on disk of a specific file, or, given a volume handle, the locations of bad clusters on a volume.
helpviewer_keywords: ["FSCTL_GET_RETRIEVAL_POINTERS","FSCTL_GET_RETRIEVAL_POINTERS control","FSCTL_GET_RETRIEVAL_POINTERS control code [Files]","_win32_fsctl_get_retrieval_pointers","base.fsctl_get_retrieval_pointers","fs.fsctl_get_retrieval_pointers","winioctl/FSCTL_GET_RETRIEVAL_POINTERS"]
old-location: fs\fsctl_get_retrieval_pointers.htm
tech.root: fs
ms.assetid: 002f6703-8db3-4034-a79f-3fa9c4159115
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_RETRIEVAL_POINTERS, FSCTL_GET_RETRIEVAL_POINTERS control, FSCTL_GET_RETRIEVAL_POINTERS control code [Files], _win32_fsctl_get_retrieval_pointers, base.fsctl_get_retrieval_pointers, fs.fsctl_get_retrieval_pointers, winioctl/FSCTL_GET_RETRIEVAL_POINTERS
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
 - FSCTL_GET_RETRIEVAL_POINTERS
 - winioctl/FSCTL_GET_RETRIEVAL_POINTERS
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
 - FSCTL_GET_RETRIEVAL_POINTERS
---

# FSCTL_GET_RETRIEVAL_POINTERS IOCTL

## -description

Given a file handle, retrieves a data structure that describes the allocation and location on disk of a specific file, or, given a volume handle, the locations of bad clusters on a volume.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
DeviceIoControl(
  (HANDLE) hDevice,                 // handle to file, directory, or volume
  FSCTL_GET_RETRIEVAL_POINTERS,     // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
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

The **FSCTL_GET_RETRIEVAL_POINTERS** operation retrieves a variably sized data structure that describes the allocation and location on disk of a specific file. The structure describes the mapping between virtual cluster numbers (VCN offsets within the file or stream space) and logical cluster numbers (LCN offsets within the volume space).

The **FSCTL_GET_RETRIEVAL_POINTERS** control code is supported for file or directory operations on NTFS, FAT, exFAT, UDF, and ReFS file systems.

On supported file systems, the **FSCTL_GET_RETRIEVAL_POINTERS** operation returns the extent locations of nonresident data.  Resident data never has extent locations.

The **FSCTL_GET_RETRIEVAL_POINTERS** control code also supports the alternate functionality of locating bad clusters. To query for the locations of bad clusters on a volume formatted with NTFS, FAT, or exFAT, use a volume handle as the *hDevice* parameter. This functionality is supported only on NTFS, FAT, and exFAT, and the caller must have **MANAGE_VOLUME_ACCESS** permission to the volume.

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [Defragmentation](/windows/desktop/FileIO/defragmenting-files)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [FSCTL_GET_RETRIEVAL_POINTER_BASE](ni-winioctl-fsctl_get_retrieval_pointer_base.md)
* [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md)
* [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md)
* [GetQueuedCompletionStatus](../ioapiset/nf-ioapiset-getqueuedcompletionstatus.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [RETRIEVAL_POINTERS_BUFFER](ns-winioctl-retrieval_pointers_buffer.md)
* [STARTING_VCN_INPUT_BUFFER](ns-winioctl-starting_vcn_input_buffer.md)
