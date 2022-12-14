---
UID: NI:winioctl.FSCTL_GET_INTEGRITY_INFORMATION
title: FSCTL_GET_INTEGRITY_INFORMATION
description: Retrieves the integrity status of a file or directory on a ReFS volume. (FSCTL_GET_INTEGRITY_INFORMATION)
helpviewer_keywords: ["FSCTL_GET_INTEGRITY_INFORMATION","FSCTL_GET_INTEGRITY_INFORMATION control","FSCTL_GET_INTEGRITY_INFORMATION control code [Files]","fs.fsctl_get_integrity_information","winioctl/FSCTL_GET_INTEGRITY_INFORMATION"]
old-location: fs\fsctl_get_integrity_information.htm
tech.root: fs
ms.assetid: 5e003b2f-d38a-45f1-9b50-40af4087b0ce
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_INTEGRITY_INFORMATION, FSCTL_GET_INTEGRITY_INFORMATION control, FSCTL_GET_INTEGRITY_INFORMATION control code [Files], fs.fsctl_get_integrity_information, winioctl/FSCTL_GET_INTEGRITY_INFORMATION
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
 - FSCTL_GET_INTEGRITY_INFORMATION
 - winioctl/FSCTL_GET_INTEGRITY_INFORMATION
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
 - FSCTL_GET_INTEGRITY_INFORMATION
---

# FSCTL_GET_INTEGRITY_INFORMATION IOCTL


## -description

Retrieves the integrity status of a file or directory on a ReFS volume.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to file or directory
  FSCTL_GET_INTEGRITY_INFORMATION,  // dwIoControlCode
  (LPDWORD) NULL,                   // pInBuffer
  (DWORD) 0,                        // InBufferSize
  (LPDWORD) pOutBuffer,             // FSCTL_GET_INTEGRITY_INFORMATION_BUFFER
  (DWORD) OutBufferSize,            // size of output buffer
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
* [FSCTL_GET_INTEGRITY_INFORMATION_BUFFER](ns-winioctl-fsctl_get_integrity_information_buffer.md)
* [FSCTL_SET_INTEGRITY_INFORMATION](ni-winioctl-fsctl_set_integrity_information.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)
