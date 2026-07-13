---
UID: NI:winioctl.IOCTL_STORAGE_PROTOCOL_COMMAND
title: IOCTL_STORAGE_PROTOCOL_COMMAND
description: Windows applications can use this control code to return properties of a storage device or adapter. The request indicates the kind of information to retrieve, such as inquiry data for a device or capabilities and limitations of an adapter.
helpviewer_keywords: ["IOCTL_STORAGE_PROTOCOL_COMMAND","IOCTL_STORAGE_PROTOCOL_COMMAND control","IOCTL_STORAGE_PROTOCOL_COMMAND control code [Files]","fs.ioctl_storage_protocol_command","winioctl/IOCTL_STORAGE_PROTOCOL_COMMAND"]
old-location: fs\ioctl_storage_protocol_command.htm
tech.root: fs
ms.assetid: 77027740-CDFD-422A-B458-C36B2E346EFD
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_PROTOCOL_COMMAND, IOCTL_STORAGE_PROTOCOL_COMMAND control, IOCTL_STORAGE_PROTOCOL_COMMAND control code [Files], fs.ioctl_storage_protocol_command, winioctl/IOCTL_STORAGE_PROTOCOL_COMMAND
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
 - IOCTL_STORAGE_PROTOCOL_COMMAND
 - winioctl/IOCTL_STORAGE_PROTOCOL_COMMAND
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - IOCTL_STORAGE_PROTOCOL_COMMAND
---

# IOCTL_STORAGE_PROTOCOL_COMMAND IOCTL


## -description

Windows applications can use **IOCTL_STORAGE_PROTOCOL_COMMAND** to conduct pass-through of protocol specific commands to the storage device or adapter. The request indicates the bus specific command which is further sent to a specific type of device to process. For more information, see the page on [working with NVMe drives](/windows/win32/fileio/working-with-nvme-devices#using-ioctl_storage_protocol_command-to-send-commands).

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_STORAGE_PROTOCOL_COMMAND,   // dwIoControlCode
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
* [STORAGE_PROPERTY_ID](ne-winioctl-storage_property_id.md)
* [STORAGE_PROPERTY_QUERY](ns-winioctl-storage_property_query.md)
