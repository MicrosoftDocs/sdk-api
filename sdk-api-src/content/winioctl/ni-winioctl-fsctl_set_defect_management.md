---
UID: NI:winioctl.FSCTL_SET_DEFECT_MANAGEMENT
title: FSCTL_SET_DEFECT_MANAGEMENT
description: Sets the software defect management state for the specified file. Used for UDF file systems.
helpviewer_keywords: ["FSCTL_SET_DEFECT_MANAGEMENT","FSCTL_SET_DEFECT_MANAGEMENT control","FSCTL_SET_DEFECT_MANAGEMENT control code [Files]","fs.fsctl_set_defect_management","winioctl/FSCTL_SET_DEFECT_MANAGEMENT"]
old-location: fs\fsctl_set_defect_management.htm
tech.root: fs
ms.assetid: 6febbce3-7e70-43c1-a75e-84addc218857
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_DEFECT_MANAGEMENT, FSCTL_SET_DEFECT_MANAGEMENT control, FSCTL_SET_DEFECT_MANAGEMENT control code [Files], fs.fsctl_set_defect_management, winioctl/FSCTL_SET_DEFECT_MANAGEMENT
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
 - FSCTL_SET_DEFECT_MANAGEMENT
 - winioctl/FSCTL_SET_DEFECT_MANAGEMENT
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
 - FSCTL_SET_DEFECT_MANAGEMENT
---

# FSCTL_SET_DEFECT_MANAGEMENT IOCTL


## -description

Sets the software defect management state for the specified file. Used for UDF file systems.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_SET_DEFECT_MANAGEMENT,      // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
  NULL,                             // output buffer
  0,                                // output buffer size
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
Cluster Shared Volume File System (CsvFS) | No
Resilient File System (ReFS) | No

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_SET_DEFECT_MGMT_BUFFER](ns-winioctl-file_set_defect_mgmt_buffer.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)