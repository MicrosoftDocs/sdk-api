---
UID: NI:winioctl.FSCTL_GET_RETRIEVAL_POINTER_BASE
title: FSCTL_GET_RETRIEVAL_POINTER_BASE
description: Returns the sector offset to the first logical cluster number (LCN) of the file system relative to the start of the volume.
helpviewer_keywords: ["FSCTL_GET_RETRIEVAL_POINTER_BASE","FSCTL_GET_RETRIEVAL_POINTER_BASE control","FSCTL_GET_RETRIEVAL_POINTER_BASE control code [Files]","fs.fsctl_get_retrieval_pointer_base","winioctl/FSCTL_GET_RETRIEVAL_POINTER_BASE"]
old-location: fs\fsctl_get_retrieval_pointer_base.htm
tech.root: fs
ms.assetid: 17925fe8-ab5a-4bfb-8d9e-cd574c024107
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_RETRIEVAL_POINTER_BASE, FSCTL_GET_RETRIEVAL_POINTER_BASE control, FSCTL_GET_RETRIEVAL_POINTER_BASE control code [Files], fs.fsctl_get_retrieval_pointer_base, winioctl/FSCTL_GET_RETRIEVAL_POINTER_BASE
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
 - FSCTL_GET_RETRIEVAL_POINTER_BASE
 - winioctl/FSCTL_GET_RETRIEVAL_POINTER_BASE
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
 - FSCTL_GET_RETRIEVAL_POINTER_BASE
---

# FSCTL_GET_RETRIEVAL_POINTER_BASE IOCTL


## -description

Returns the sector offset to the first logical cluster number (LCN) of the file system relative to the start of the volume.


To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.
   
```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                    // handle to volume
  FSCTL_GET_RETRIEVAL_POINTER_BASE,    // dwIoControlCode
  (LPVOID) NULL,                       // input buffer
  (DWORD) 0,                           // size of input buffer
  (LPVOID) lpOutBuffer,                // output buffer
  (DWORD) nOutBufferSize,              // size of output buffer
  (LPDWORD) lpBytesReturned,           // number of bytes returned
  (LPOVERLAPPED) lpOverlapped          // OVERLAPPED structure
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

Adding the value retrieved by **FSCTL_GET_RETRIEVAL_POINTER_BASE** to the value retrieved by the [FSCTL_GET_RETRIEVAL_POINTERS](ni-winioctl-fsctl_get_retrieval_pointers.md) control code results in a volume-relative file extent offset. 

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

## -see-also

* [Clusters and Extents](/windows/desktop/FileIO/clusters-and-extents)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)