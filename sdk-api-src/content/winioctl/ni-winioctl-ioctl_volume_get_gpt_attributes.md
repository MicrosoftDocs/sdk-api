---
UID: NI:winioctl.IOCTL_VOLUME_GET_GPT_ATTRIBUTES
title: IOCTL_VOLUME_GET_GPT_ATTRIBUTES
description: Retrieves the attributes for a volume.
helpviewer_keywords: ["IOCTL_VOLUME_GET_GPT_ATTRIBUTES","IOCTL_VOLUME_GET_GPT_ATTRIBUTES control","IOCTL_VOLUME_GET_GPT_ATTRIBUTES control code [Files]","fs.ioctl_volume_get_gpt_attributes","winioctl/IOCTL_VOLUME_GET_GPT_ATTRIBUTES"]
old-location: fs\ioctl_volume_get_gpt_attributes.htm
tech.root: fs
ms.assetid: 3e58e0d6-215a-47f3-b1bf-e8d53c224b68
ms.date: 12/05/2018
ms.keywords: IOCTL_VOLUME_GET_GPT_ATTRIBUTES, IOCTL_VOLUME_GET_GPT_ATTRIBUTES control, IOCTL_VOLUME_GET_GPT_ATTRIBUTES control code [Files], fs.ioctl_volume_get_gpt_attributes, winioctl/IOCTL_VOLUME_GET_GPT_ATTRIBUTES
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
 - IOCTL_VOLUME_GET_GPT_ATTRIBUTES
 - winioctl/IOCTL_VOLUME_GET_GPT_ATTRIBUTES
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
 - IOCTL_VOLUME_GET_GPT_ATTRIBUTES
---

# IOCTL_VOLUME_GET_GPT_ATTRIBUTES IOCTL


## -description

Retrieves the attributes for a volume.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to the volume device
  IOCTL_VOLUME_GET_GPT_ATTRIBUTES,  // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  (LPVOID) lpOutBuffer,             // output buffer
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
* [VOLUME_GET_GPT_ATTRIBUTES_INFORMATION](ns-winioctl-volume_get_gpt_attributes_information.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)