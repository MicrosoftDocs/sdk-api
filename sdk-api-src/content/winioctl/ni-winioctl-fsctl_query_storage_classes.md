---
UID: NI:winioctl.FSCTL_QUERY_STORAGE_CLASSES
title: FSCTL_QUERY_STORAGE_CLASSES
description: Retrieves the storage tiers defined for a volume that supports data tiering.
helpviewer_keywords: ["FSCTL_QUERY_STORAGE_CLASSES","FSCTL_QUERY_STORAGE_CLASSES control","FSCTL_QUERY_STORAGE_CLASSES control code [Files]","fs.fsctl_query_storage_classes","winioctl/FSCTL_QUERY_STORAGE_CLASSES"]
old-location: fs\fsctl_query_storage_classes.htm
tech.root: fs
ms.assetid: E624CBB4-F788-4FC9-B134-8C4562F21E44
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_STORAGE_CLASSES, FSCTL_QUERY_STORAGE_CLASSES control, FSCTL_QUERY_STORAGE_CLASSES control code [Files], fs.fsctl_query_storage_classes, winioctl/FSCTL_QUERY_STORAGE_CLASSES
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
 - FSCTL_QUERY_STORAGE_CLASSES
 - winioctl/FSCTL_QUERY_STORAGE_CLASSES
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
 - FSCTL_QUERY_STORAGE_CLASSES
---

# FSCTL_QUERY_STORAGE_CLASSES IOCTL


## -description

Retrieves the storage tiers defined for a volume that supports data tiering.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_QUERY_STORAGE_CLASSES,      // dwIoControlCode
  (LPDWORD) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
  (LPDWORD) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
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

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)