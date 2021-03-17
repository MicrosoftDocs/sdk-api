---
UID: NI:winioctl.FSCTL_MAKE_MEDIA_COMPATIBLE
title: FSCTL_MAKE_MEDIA_COMPATIBLE
description: Closes an open UDF session on write-once media to make the media ROM compatible.
helpviewer_keywords: ["FSCTL_MAKE_MEDIA_COMPATIBLE","FSCTL_MAKE_MEDIA_COMPATIBLE control","FSCTL_MAKE_MEDIA_COMPATIBLE control code [Files]","fs.fsctl_make_media_compatible","winioctl/FSCTL_MAKE_MEDIA_COMPATIBLE"]
old-location: fs\fsctl_make_media_compatible.htm
tech.root: fs
ms.assetid: bbe58c35-d0da-4c29-a412-a84a138dc9fb
ms.date: 12/05/2018
ms.keywords: FSCTL_MAKE_MEDIA_COMPATIBLE, FSCTL_MAKE_MEDIA_COMPATIBLE control, FSCTL_MAKE_MEDIA_COMPATIBLE control code [Files], fs.fsctl_make_media_compatible, winioctl/FSCTL_MAKE_MEDIA_COMPATIBLE
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
 - FSCTL_MAKE_MEDIA_COMPATIBLE
 - winioctl/FSCTL_MAKE_MEDIA_COMPATIBLE
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
 - FSCTL_MAKE_MEDIA_COMPATIBLE
---

# FSCTL_MAKE_MEDIA_COMPATIBLE IOCTL


## -description

Closes an open UDF session on write-once media to make the media ROM compatible. Used in conjunction with **FILE_SEQUENTIAL_WRITE_ONCE** volume flag. This call must be issued on the volume handle.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to device
  FSCTL_MAKE_MEDIA_COMPATIBLE,   // dwIoControlCode
  (LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // output buffer
  0,                             // size of output buffer
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
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

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | No
Resilient File System (ReFS) | No

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_MAKE_COMPATIBLE_BUFFER](ns-winioctl-file_make_compatible_buffer.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)