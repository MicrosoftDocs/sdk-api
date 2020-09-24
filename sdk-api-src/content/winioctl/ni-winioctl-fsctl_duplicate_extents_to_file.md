---
UID: NI:winioctl.FSCTL_DUPLICATE_EXTENTS_TO_FILE
title: FSCTL_DUPLICATE_EXTENTS_TO_FILE
description: Instructs the file system to copy a range of file bytes on behalf of an application.
helpviewer_keywords: ["FSCTL_DUPLICATE_EXTENTS_TO_FILE","FSCTL_DUPLICATE_EXTENTS_TO_FILE control","FSCTL_DUPLICATE_EXTENTS_TO_FILE control code [Files]","fs.fsctl_duplicate_extents_to_file","winioctl/FSCTL_DUPLICATE_EXTENTS_TO_FILE"]
old-location: fs\fsctl_duplicate_extents_to_file.htm
tech.root: fs
ms.assetid: D66D2172-9308-4138-A321-867589787FED
ms.date: 12/05/2018
ms.keywords: FSCTL_DUPLICATE_EXTENTS_TO_FILE, FSCTL_DUPLICATE_EXTENTS_TO_FILE control, FSCTL_DUPLICATE_EXTENTS_TO_FILE control code [Files], fs.fsctl_duplicate_extents_to_file, winioctl/FSCTL_DUPLICATE_EXTENTS_TO_FILE
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - FSCTL_DUPLICATE_EXTENTS_TO_FILE
 - winioctl/FSCTL_DUPLICATE_EXTENTS_TO_FILE
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
 - FSCTL_DUPLICATE_EXTENTS_TO_FILE
---

# FSCTL_DUPLICATE_EXTENTS_TO_FILE IOCTL


## -description

Instructs the file system to copy a range of file bytes on behalf of an application. The destination file may be the same as, or different from, the source file. See [Block Cloning](/windows/desktop/FileIO/block-cloning) for more information.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE)       hDevice,           // handle to device
  FSCTL_DUPLICATE_EXTENTS_TO_FILE,  // dwIoControlCode
  (LPVOID)       lpInBuffer,        // input buffer
  (DWORD)        nInBufferSize,     // size of input buffer
  NULL,                             // lpOutBuffer
  0,                                // nOutBufferSize
  (LPDWORD)      lpBytesReturned,   // number of bytes returned
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

See [Block Cloning](/windows/desktop/FileIO/block-cloning) for more information on this operation.

In Windows Server 2016, this function is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.1.1 protocol | Yes
SMB 3.1.1 Transparent Failover (TFO) | Yes
SMB 3.1.1 with Scale-out File Shares (SoFS) | Yes
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | Yes

## -see-also

* [Block Cloning](/windows/desktop/FileIO/block-cloning)
* [DUPLICATE_EXTENTS_DATA](../winioctl/ns-winioctl-duplicate_extents_data.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)