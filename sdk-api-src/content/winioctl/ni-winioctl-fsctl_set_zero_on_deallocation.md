---
UID: NI:winioctl.FSCTL_SET_ZERO_ON_DEALLOCATION
title: FSCTL_SET_ZERO_ON_DEALLOCATION
description: Indicates an NTFS file system file handle should have its clusters filled with zeros when it is deallocated.
helpviewer_keywords: ["FSCTL_SET_ZERO_ON_DEALLOCATION","FSCTL_SET_ZERO_ON_DEALLOCATION control","FSCTL_SET_ZERO_ON_DEALLOCATION control code [Files]","fs.fsctl_set_zero_on_deallocation","winioctl/FSCTL_SET_ZERO_ON_DEALLOCATION"]
old-location: fs\fsctl_set_zero_on_deallocation.htm
tech.root: fs
ms.assetid: dc926f24-de52-431b-bac2-f97535de6848
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_ZERO_ON_DEALLOCATION, FSCTL_SET_ZERO_ON_DEALLOCATION control, FSCTL_SET_ZERO_ON_DEALLOCATION control code [Files], fs.fsctl_set_zero_on_deallocation, winioctl/FSCTL_SET_ZERO_ON_DEALLOCATION
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
 - FSCTL_SET_ZERO_ON_DEALLOCATION
 - winioctl/FSCTL_SET_ZERO_ON_DEALLOCATION
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
 - FSCTL_SET_ZERO_ON_DEALLOCATION
---

# FSCTL_SET_ZERO_ON_DEALLOCATION IOCTL


## -description

Indicates an NTFS file system file handle should have its clusters filled with zeros when it is deallocated. If a file is resident, it is converted to nonresident. When clusters are deallocated, the clusters on a disk are zeroed. If a file is deleted, all clusters associated with the file are zeroed.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_SET_ZERO_ON_DEALLOCATION,   // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
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

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | Yes
SMB 3.0 with Scale-out File Shares (SO) | Yes
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | No

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)