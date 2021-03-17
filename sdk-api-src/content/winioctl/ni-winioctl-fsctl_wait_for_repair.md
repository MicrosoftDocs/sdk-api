---
UID: NI:winioctl.FSCTL_WAIT_FOR_REPAIR
title: FSCTL_WAIT_FOR_REPAIR
description: Returns when the specified repairs are completed.
helpviewer_keywords: ["FSCTL_WAIT_FOR_REPAIR","FSCTL_WAIT_FOR_REPAIR control","FSCTL_WAIT_FOR_REPAIR control code [Files]","fs.fsctl_wait_for_repair","winioctl/FSCTL_WAIT_FOR_REPAIR"]
old-location: fs\fsctl_wait_for_repair.htm
tech.root: fs
ms.assetid: 593ca2f0-1455-4b46-925a-61ad07f8fb5c
ms.date: 12/05/2018
ms.keywords: FSCTL_WAIT_FOR_REPAIR, FSCTL_WAIT_FOR_REPAIR control, FSCTL_WAIT_FOR_REPAIR control code [Files], fs.fsctl_wait_for_repair, winioctl/FSCTL_WAIT_FOR_REPAIR
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
 - FSCTL_WAIT_FOR_REPAIR
 - winioctl/FSCTL_WAIT_FOR_REPAIR
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
 - FSCTL_WAIT_FOR_REPAIR
---

# FSCTL_WAIT_FOR_REPAIR IOCTL


## -description

Returns when the specified repairs are completed.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_WAIT_FOR_REPAIR,        // dwIoControlCode
  (PUSHORT) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  NULL,                         // lpOutBuffer
  0,                            // nOutBufferSize
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
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | No

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_GET_REPAIR](ni-winioctl-fsctl_get_repair.md)
* [FSCTL_INITIATE_REPAIR](ni-winioctl-fsctl_initiate_repair.md)
* [FSCTL_SET_REPAIR](ni-winioctl-fsctl_set_repair.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)