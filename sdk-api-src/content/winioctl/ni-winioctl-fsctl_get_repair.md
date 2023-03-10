---
UID: NI:winioctl.FSCTL_GET_REPAIR
title: FSCTL_GET_REPAIR
description: Retrieves information about the NTFS file system's self-healing mechanism.
helpviewer_keywords: ["FSCTL_GET_REPAIR","FSCTL_GET_REPAIR control","FSCTL_GET_REPAIR control code [Files]","fs.fsctl_get_repair","winioctl/FSCTL_GET_REPAIR"]
old-location: fs\fsctl_get_repair.htm
tech.root: fs
ms.assetid: 25c9ffdf-2839-46aa-b1fe-ce1383a3a813
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_REPAIR, FSCTL_GET_REPAIR control, FSCTL_GET_REPAIR control code [Files], fs.fsctl_get_repair, winioctl/FSCTL_GET_REPAIR
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
 - FSCTL_GET_REPAIR
 - winioctl/FSCTL_GET_REPAIR
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
 - FSCTL_GET_REPAIR
---

# FSCTL_GET_REPAIR IOCTL


## -description

Retrieves information about the NTFS file system's self-healing mechanism.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to device
  FSCTL_GET_REPAIR,              // dwIoControlCode
  NULL,                          // lpInBuffer
  0,                             // nInBufferSize
  (ULONG) lpOutBuffer,           // output buffer
  (DWORD) nOutBufferSize,        // size of output buffer
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
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | No

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_INITIATE_REPAIR](ni-winioctl-fsctl_initiate_repair.md)
* [FSCTL_SET_REPAIR](ni-winioctl-fsctl_set_repair.md)
* [FSCTL_WAIT_FOR_REPAIR](ni-winioctl-fsctl_wait_for_repair.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)