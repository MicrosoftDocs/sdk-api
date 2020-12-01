---
UID: NI:winioctl.FSCTL_QUERY_FILE_SYSTEM_RECOGNITION
title: FSCTL_QUERY_FILE_SYSTEM_RECOGNITION
description: Queries for file system recognition information on a volume.
helpviewer_keywords: ["FSCTL_QUERY_FILE_SYSTEM_RECOGNITION","FSCTL_QUERY_FILE_SYSTEM_RECOGNITION control","FSCTL_QUERY_FILE_SYSTEM_RECOGNITION control code [Files]","fs.fsctl_query_file_system_recognition","winioctl/FSCTL_QUERY_FILE_SYSTEM_RECOGNITION"]
old-location: fs\fsctl_query_file_system_recognition.htm
tech.root: fs
ms.assetid: 0b2ff131-a659-4bd0-b329-41fb60edbe13
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_FILE_SYSTEM_RECOGNITION, FSCTL_QUERY_FILE_SYSTEM_RECOGNITION control, FSCTL_QUERY_FILE_SYSTEM_RECOGNITION control code [Files], fs.fsctl_query_file_system_recognition, winioctl/FSCTL_QUERY_FILE_SYSTEM_RECOGNITION
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - FSCTL_QUERY_FILE_SYSTEM_RECOGNITION
 - winioctl/FSCTL_QUERY_FILE_SYSTEM_RECOGNITION
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
 - FSCTL_QUERY_FILE_SYSTEM_RECOGNITION
---

# FSCTL_QUERY_FILE_SYSTEM_RECOGNITION IOCTL


## -description

Queries for file system recognition information on a volume.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                     // handle to volume
  FSCTL_QUERY_FILE_SYSTEM_RECOGNITION,  // dwIoControlCode
  NULL,                                 // lpInBuffer
  0,                                    // nInBufferSize
  (LPVOID) lpOutBuffer,                 // output buffer
  (DWORD) nOutBufferSize,               // size of output buffer
  (LPDWORD) lpBytesReturned,            // number of bytes returned
  (LPOVERLAPPED) lpOverlapped           // OVERLAPPED structure
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

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_SYSTEM_RECOGNITION_INFORMATION](ns-winioctl-file_system_recognition_information.md)
* [FILE_SYSTEM_RECOGNITION_STRUCTURE](/windows/desktop/FileIO/file-system-recognition-structure)
* [File System Recognition](/windows/desktop/FileIO/file-system-recognition)