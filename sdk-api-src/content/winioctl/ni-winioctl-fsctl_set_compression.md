---
UID: NI:winioctl.FSCTL_SET_COMPRESSION
title: FSCTL_SET_COMPRESSION
description: Sets the compression state of a file or directory on a volume whose file system supports per-file and per-directory compression.
helpviewer_keywords: ["COMPRESSION_FORMAT_DEFAULT","COMPRESSION_FORMAT_LZNT1","COMPRESSION_FORMAT_NONE","FSCTL_SET_COMPRESSION","FSCTL_SET_COMPRESSION control","FSCTL_SET_COMPRESSION control code [Files]","_win32_fsctl_set_compression","all other values","base.fsctl_set_compression","fs.fsctl_set_compression","winioctl/FSCTL_SET_COMPRESSION"]
old-location: fs\fsctl_set_compression.htm
tech.root: fs
ms.assetid: e6fb29ed-f4f4-4507-8312-d771ffb00256
ms.date: 12/05/2018
ms.keywords: COMPRESSION_FORMAT_DEFAULT, COMPRESSION_FORMAT_LZNT1, COMPRESSION_FORMAT_NONE, FSCTL_SET_COMPRESSION, FSCTL_SET_COMPRESSION control, FSCTL_SET_COMPRESSION control code [Files], _win32_fsctl_set_compression, all other values, base.fsctl_set_compression, fs.fsctl_set_compression, winioctl/FSCTL_SET_COMPRESSION
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
 - FSCTL_SET_COMPRESSION
 - winioctl/FSCTL_SET_COMPRESSION
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
 - FSCTL_SET_COMPRESSION
---

# FSCTL_SET_COMPRESSION IOCTL


## -description

Sets the compression state of a file or directory on a volume whose file system supports per-file and per-directory compression. You can use **FSCTL_SET_COMPRESSION** to compress or uncompress a file or directory on such a volume.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to file or directory
  FSCTL_SET_COMPRESSION,            // dwIoControlCode
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

The LZNT1 compression algorithm is the only compression algorithm implemented. As a result, the LZNT1 compression algorithm is used as the DEFAULT compression method.

If the file system of the volume containing the specified file or directory does not support per-file or per-directory compression, the operation fails.

The compression state change of the file or directory occurs synchronously with the call to [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md).

To retrieve the compression state of a file or directory, use the [FSCTL_GET_COMPRESSION](ni-winioctl-fsctl_get_compression.md) control code.

To retrieve the compression attribute of a file or directory, use the [GetFileAttributes](../fileapi/nf-fileapi-getfileattributesa.md) function. The compression attribute indicates whether a file or directory is compressed. The compression state indicates whether a file or directory is compressed and, if it is, the format of the compressed data.

Directories are not actually compressed by this operation. Rather, the operation sets the default state for files created in the directory to be compressed.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use unbuffered I/O.

File compression is supported for files of a maximum uncompressed size of 30 gigabytes.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | See comment
Resilient File System (ReFS) | No

CsvFs does not support making a directory compressed. CsvFs allows making file compressed only when the file is opened exclusively by a node. SMB 3.0 Transparent Failover and Scale-Out does not support NTFS compressed files. The FSCTL call is not blocked, but is unsupported."


<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
You cannot change the compression state of a file  opened with 
      <a href="/windows/desktop/api/winbase/nf-winbase-createfiletransacteda">CreateFileTransacted</a>.

For more information about transactions, see 
      <a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_GET_COMPRESSION](ni-winioctl-fsctl_get_compression.md)
* [File Compression and Decompression](/windows/desktop/FileIO/file-compression-and-decompression)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)
* [GetFileAttributes](../fileapi/nf-fileapi-getfileattributesa.md)
* [Transactional NTFS](/windows/desktop/FileIO/transactional-ntfs-portal)