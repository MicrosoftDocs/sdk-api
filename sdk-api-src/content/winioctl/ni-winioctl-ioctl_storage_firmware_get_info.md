---
UID: NI:winioctl.IOCTL_STORAGE_FIRMWARE_GET_INFO
title: IOCTL_STORAGE_FIRMWARE_GET_INFO
description: Windows applications can use this control code to query the storage device for detailed firmware information.
helpviewer_keywords: ["IOCTL_STORAGE_FIRMWARE_GET_INFO","IOCTL_STORAGE_FIRMWARE_GET_INFO control","IOCTL_STORAGE_FIRMWARE_GET_INFO control code [Files]","fs.ioctl_storage_firmware_get_info","winioctl/IOCTL_STORAGE_FIRMWARE_GET_INFO"]
old-location: fs\ioctl_storage_firmware_get_info.htm
tech.root: fs
ms.assetid: DBF40C42-2282-4F0E-B83A-D3154D7EF332
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_FIRMWARE_GET_INFO, IOCTL_STORAGE_FIRMWARE_GET_INFO control, IOCTL_STORAGE_FIRMWARE_GET_INFO control code [Files], fs.ioctl_storage_firmware_get_info, winioctl/IOCTL_STORAGE_FIRMWARE_GET_INFO
f1_keywords:
- winioctl/IOCTL_STORAGE_FIRMWARE_GET_INFO
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinIoctl.h
api_name:
- IOCTL_STORAGE_FIRMWARE_GET_INFO
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_FIRMWARE_GET_INFO IOCTL

## -description

Windows applications can use this control code to query the storage device for detailed firmware information. A successful call will return information about firmware revisions, activity status, as well as read/write attributes for each slot. The amount of data returned will vary based on storage protocol.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_STORAGE_FIRMWARE_GET_INFO,  // dwIoControlCode
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).


## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [IOCTL_STORAGE_FIRMWARE_ACTIVATE](ni-winioctl-ioctl_storage_firmware_activate.md)
* [IOCTL_STORAGE_FIRMWARE_DOWNLOAD](ni-winioctl-ioctl_storage_firmware_download.md)
* [STORAGE_HW_FIRMWARE_ACTIVATE](ns-winioctl-storage_hw_firmware_activate.md)
* [STORAGE_HW_FIRMWARE_DOWNLOAD](ns-winioctl-storage_hw_firmware_download.md)
* [STORAGE_HW_FIRMWARE_INFO](https://docs.microsoft.com/windows/desktop/FileIO/storage-hw-firmware-info)
* [STORAGE_HW_FIRMWARE_INFO_QUERY](https://docs.microsoft.com/windows/desktop/FileIO/storage-hw-firmware-info-query)
* [STORAGE_HW_FIRMWARE_SLOT_INFO](https://docs.microsoft.com/windows/desktop/FileIO/storage-hw-firmware-slot-info)
