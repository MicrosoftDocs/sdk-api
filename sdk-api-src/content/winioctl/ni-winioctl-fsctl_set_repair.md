---
UID: NI:winioctl.FSCTL_SET_REPAIR
title: FSCTL_SET_REPAIR
description: Sets the mode of an NTFS file system's self-healing capability.
helpviewer_keywords: ["FSCTL_SET_REPAIR","FSCTL_SET_REPAIR control","FSCTL_SET_REPAIR control code [Files]","SET_REPAIR_DELETE_CROSSLINK","SET_REPAIR_DISABLED_AND_BUGCHECK_ON_CORRUPT","SET_REPAIR_ENABLED","SET_REPAIR_VOLUME_BITMAP_SCAN","SET_REPAIR_WARN_ABOUT_DATA_LOSS","fs.fsctl_set_repair","winioctl/FSCTL_SET_REPAIR"]
old-location: fs\fsctl_set_repair.htm
tech.root: fs
ms.assetid: 3df03a87-7117-4f85-a04e-54bcd800e8ff
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_REPAIR, FSCTL_SET_REPAIR control, FSCTL_SET_REPAIR control code [Files], SET_REPAIR_DELETE_CROSSLINK, SET_REPAIR_DISABLED_AND_BUGCHECK_ON_CORRUPT, SET_REPAIR_ENABLED, SET_REPAIR_VOLUME_BITMAP_SCAN, SET_REPAIR_WARN_ABOUT_DATA_LOSS, fs.fsctl_set_repair, winioctl/FSCTL_SET_REPAIR
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
 - FSCTL_SET_REPAIR
 - winioctl/FSCTL_SET_REPAIR
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
 - FSCTL_SET_REPAIR
---

# FSCTL_SET_REPAIR IOCTL


## -description

Sets the mode of an NTFS file system's self-healing capability.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SET_REPAIR,             // dwIoControlCode
  (PUSHORT) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  NULL,                         // not used
  0,                            // not used
  (LPDWORD) lpBytesReturned,    // bytes returned
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
* [FSCTL_WAIT_FOR_REPAIR](ni-winioctl-fsctl_wait_for_repair.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)