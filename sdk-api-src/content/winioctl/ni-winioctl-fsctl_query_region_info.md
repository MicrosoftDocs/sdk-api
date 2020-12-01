---
UID: NI:winioctl.FSCTL_QUERY_REGION_INFO
title: FSCTL_QUERY_REGION_INFO
description: Retrieves the storage tier regions defined for a volume that supports data tiering.
helpviewer_keywords: ["FSCTL_QUERY_REGION_INFO","FSCTL_QUERY_REGION_INFO control","FSCTL_QUERY_REGION_INFO control code [Files]","fs.fsctl_query_region_info","winioctl/FSCTL_QUERY_REGION_INFO"]
old-location: fs\fsctl_query_region_info.htm
tech.root: fs
ms.assetid: 292D377B-F7DE-489B-B686-0CE5278360BC
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_REGION_INFO, FSCTL_QUERY_REGION_INFO control, FSCTL_QUERY_REGION_INFO control code [Files], fs.fsctl_query_region_info, winioctl/FSCTL_QUERY_REGION_INFO
req.header: winioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
 - FSCTL_QUERY_REGION_INFO
 - winioctl/FSCTL_QUERY_REGION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoctl.h
api_name:
 - FSCTL_QUERY_REGION_INFO
---

# FSCTL_QUERY_REGION_INFO IOCTL


## -description

Retrieves the storage tier regions defined for a volume that supports data tiering.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_QUERY_REGION_INFO,      // dwIoControlCode
  (LPDWORD) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPDWORD) lpOutBuffer,        // output buffer
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

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)