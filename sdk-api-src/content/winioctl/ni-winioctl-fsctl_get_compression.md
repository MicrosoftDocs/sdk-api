---
UID: NI:winioctl.FSCTL_GET_COMPRESSION
title: FSCTL_GET_COMPRESSION
description: Retrieves the current compression state of a file or directory on a volume whose file system supports per-stream compression.
helpviewer_keywords: ["COMPRESSION_FORMAT_LZNT1","COMPRESSION_FORMAT_NONE","FSCTL_GET_COMPRESSION","FSCTL_GET_COMPRESSION control","FSCTL_GET_COMPRESSION control code [Files]","_win32_fsctl_get_compression","all other values","base.fsctl_get_compression","fs.fsctl_get_compression","winioctl/FSCTL_GET_COMPRESSION"]
old-location: fs\fsctl_get_compression.htm
tech.root: fs
ms.assetid: c9932867-4b86-4119-ad13-f99aadfa559a
ms.date: 12/05/2018
ms.keywords: COMPRESSION_FORMAT_LZNT1, COMPRESSION_FORMAT_NONE, FSCTL_GET_COMPRESSION, FSCTL_GET_COMPRESSION control, FSCTL_GET_COMPRESSION control code [Files], _win32_fsctl_get_compression, all other values, base.fsctl_get_compression, fs.fsctl_get_compression, winioctl/FSCTL_GET_COMPRESSION
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
 - FSCTL_GET_COMPRESSION
 - winioctl/FSCTL_GET_COMPRESSION
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
 - FSCTL_GET_COMPRESSION
---

# FSCTL_GET_COMPRESSION IOCTL


## -description

Retrieves the current compression state of a file or directory on a volume whose file system supports per-stream compression.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to file
  FSCTL_GET_COMPRESSION,        // dwIoControlCode
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

The LZNT1 compression algorithm is the only compression algorithm implemented.

COMPRESSION_FORMAT_DEFAULT is not a compression state so it is not included in the table under the *lpOutBuffer* parameter. This value is only used with the [FSCTL_SET_COMPRESSION](ni-winioctl-fsctl_set_compression.md) control code.

If the file system of the volume containing the specified file or directory does not support per-file or per-directory compression, the operation fails.

You can set the compression state of a file or directory by using the [FSCTL_SET_COMPRESSION](ni-winioctl-fsctl_set_compression.md) control code. You can also compress or uncompress a file using this control code.

You can retrieve the compression attribute of a file or directory by calling the [GetFileAttributes](../fileapi/nf-fileapi-getfileattributesa.md) function. The compression attribute indicates whether a file or directory is compressed. The compression state indicates whether a file or directory is compressed, and, if it is, the format of the compressed data.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | No

SMB 3.0 Transparent Failover and Scale-Out do not support NTFS compressed files. The FSCTL call is not blocked, but unsupported.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_SET_COMPRESSION](ni-winioctl-fsctl_set_compression.md)
* [File Compression and Decompression](/windows/desktop/FileIO/file-compression-and-decompression)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)
* [GetFileAttributes](../fileapi/nf-fileapi-getfileattributesa.md)