---
UID: NI:winioctl.FSCTL_READ_FROM_PLEX
title: FSCTL_READ_FROM_PLEX
description: Reads from the specified plex.
helpviewer_keywords: ["FSCTL_READ_FROM_PLEX","FSCTL_READ_FROM_PLEX control","FSCTL_READ_FROM_PLEX control code [Files]","_win32_fsctl_read_from_plex","base.fsctl_read_from_plex","fs.fsctl_read_from_plex","winioctl/FSCTL_READ_FROM_PLEX"]
old-location: fs\fsctl_read_from_plex.htm
tech.root: fs
ms.assetid: f2cddd4d-cb58-484c-9a85-274b88ec4ece
ms.date: 12/05/2018
ms.keywords: FSCTL_READ_FROM_PLEX, FSCTL_READ_FROM_PLEX control, FSCTL_READ_FROM_PLEX control code [Files], _win32_fsctl_read_from_plex, base.fsctl_read_from_plex, fs.fsctl_read_from_plex, winioctl/FSCTL_READ_FROM_PLEX
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
 - FSCTL_READ_FROM_PLEX
 - winioctl/FSCTL_READ_FROM_PLEX
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
 - FSCTL_READ_FROM_PLEX
---

# FSCTL_READ_FROM_PLEX IOCTL


## -description

Reads from the specified plex. It coordinates the read operation with the underlying dynamic volume manager.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to volume
  FSCTL_READ_FROM_PLEX,         // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
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

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | No

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [PLEX_READ_DATA_REQUEST](ns-winioctl-plex_read_data_request.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)