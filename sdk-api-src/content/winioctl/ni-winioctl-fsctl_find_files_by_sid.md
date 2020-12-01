---
UID: NI:winioctl.FSCTL_FIND_FILES_BY_SID
title: FSCTL_FIND_FILES_BY_SID
description: Searches a directory for a file whose creator owner matches the specified SID.
helpviewer_keywords: ["FSCTL_FIND_FILES_BY_SID","FSCTL_FIND_FILES_BY_SID control","FSCTL_FIND_FILES_BY_SID control code [Files]","base.fsctl_find_files_by_sid","fs.fsctl_find_files_by_sid","winioctl/FSCTL_FIND_FILES_BY_SID"]
old-location: fs\fsctl_find_files_by_sid.htm
tech.root: fs
ms.assetid: 10d46c2e-9403-4c8a-8847-f427fbc6c905
ms.date: 12/05/2018
ms.keywords: FSCTL_FIND_FILES_BY_SID, FSCTL_FIND_FILES_BY_SID control, FSCTL_FIND_FILES_BY_SID control code [Files], base.fsctl_find_files_by_sid, fs.fsctl_find_files_by_sid, winioctl/FSCTL_FIND_FILES_BY_SID
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
 - FSCTL_FIND_FILES_BY_SID
 - winioctl/FSCTL_FIND_FILES_BY_SID
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
 - FSCTL_FIND_FILES_BY_SID
---

# FSCTL_FIND_FILES_BY_SID IOCTL


## -description

Searches a directory for a file whose creator owner matches the specified SID.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to volume
  FSCTL_FIND_FILES_BY_SID,      // dwIoControlCode
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

This control code requires the use of [disk quotas](/windows/desktop/FileIO/managing-disk-quotas) on the volume.

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
* [FIND_BY_SID_DATA](ns-winioctl-find_by_sid_data.md)
* [FIND_BY_SID_OUTPUT](ns-winioctl-find_by_sid_output.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)