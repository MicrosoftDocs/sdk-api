---
UID: NI:winioctl.FSCTL_GET_BOOT_AREA_INFO
title: FSCTL_GET_BOOT_AREA_INFO
description: Retrieves the locations of boot sectors for a volume.
helpviewer_keywords: ["FSCTL_GET_BOOT_AREA_INFO","FSCTL_GET_BOOT_AREA_INFO control","FSCTL_GET_BOOT_AREA_INFO control code [Files]","fs.fsctl_get_boot_area_info","winioctl/FSCTL_GET_BOOT_AREA_INFO"]
old-location: fs\fsctl_get_boot_area_info.htm
tech.root: fs
ms.assetid: 5739354b-5342-4be9-ac50-bb983d51587c
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_BOOT_AREA_INFO, FSCTL_GET_BOOT_AREA_INFO control, FSCTL_GET_BOOT_AREA_INFO control code [Files], fs.fsctl_get_boot_area_info, winioctl/FSCTL_GET_BOOT_AREA_INFO
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
 - FSCTL_GET_BOOT_AREA_INFO
 - winioctl/FSCTL_GET_BOOT_AREA_INFO
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
 - FSCTL_GET_BOOT_AREA_INFO
---

# FSCTL_GET_BOOT_AREA_INFO IOCTL


## -description

Retrieves the locations of boot sectors for a volume. 

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to volume
  FSCTL_GET_BOOT_AREA_INFO,      // dwIoControlCode
  NULL,                          // input buffer
  0,                             // size of input buffer
  (LPVOID) lpOutBuffer,          // output buffer
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

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)