---
UID: NI:winioctl.FSCTL_REPAIR_COPIES
title: FSCTL_REPAIR_COPIES
description: Repair data corruption by selecting the proper copy to use.
helpviewer_keywords: ["FSCTL_REPAIR_COPIES","FSCTL_REPAIR_COPIES control","FSCTL_REPAIR_COPIES control code [Files]","fs.fsctl_repair_copies","winioctl/FSCTL_REPAIR_COPIES"]
old-location: fs\fsctl_repair_copies.htm
tech.root: fs
ms.assetid: 1970ed09-5f37-4cc9-98c5-982629676fe4
ms.date: 12/05/2018
ms.keywords: FSCTL_REPAIR_COPIES, FSCTL_REPAIR_COPIES control, FSCTL_REPAIR_COPIES control code [Files], fs.fsctl_repair_copies, winioctl/FSCTL_REPAIR_COPIES
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - FSCTL_REPAIR_COPIES
 - winioctl/FSCTL_REPAIR_COPIES
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
 - FSCTL_REPAIR_COPIES
---

# FSCTL_REPAIR_COPIES IOCTL


## -description

Repair data corruption by selecting the proper copy to use. This control code was introduced in Windows 8 and Windows Server 2012 for use on Storage Spaces and Streams on NTFS and ReFS and non-integrity streams on ReFS (streams with integrity on ReFS handle this automatically.)

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE)  hDevice,                // handle to file or directory
  FSCTL_REPAIR_COPIES,              // dwIoControlCode
  (LPDWORD) pInBuffer,              // REPAIR_COPIES_INPUT
  (DWORD)   InBufferSize,           // size of input buffer
  (LPDWORD) pOutBuffer,             // REPAIR_COPIES_OUTPUT
  (DWORD)   OutBufferSize,          // size of output buffer
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
* [FSCTL_GET_INTEGRITY_INFORMATION](ni-winioctl-fsctl_get_integrity_information.md)
* [REPAIR_COPIES_OUTPUT](ns-winioctl-repair_copies_output.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)