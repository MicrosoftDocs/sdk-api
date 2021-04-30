---
UID: NI:winioctl.IOCTL_CHANGER_QUERY_VOLUME_TAGS
title: IOCTL_CHANGER_QUERY_VOLUME_TAGS
description: Retrieves the volume tag information for the specified elements.
helpviewer_keywords: ["IOCTL_CHANGER_QUERY_VOLUME_TAGS","IOCTL_CHANGER_QUERY_VOLUME_TAGS control","IOCTL_CHANGER_QUERY_VOLUME_TAGS control code","_win32_ioctl_changer_query_volume_tags","base.ioctl_changer_query_volume_tags","winioctl/IOCTL_CHANGER_QUERY_VOLUME_TAGS"]
old-location: base\ioctl_changer_query_volume_tags.htm
tech.root: base
ms.assetid: 67c440e1-cef8-459d-b811-0b483ff51e7e
ms.date: 12/05/2018
ms.keywords: IOCTL_CHANGER_QUERY_VOLUME_TAGS, IOCTL_CHANGER_QUERY_VOLUME_TAGS control, IOCTL_CHANGER_QUERY_VOLUME_TAGS control code, _win32_ioctl_changer_query_volume_tags, base.ioctl_changer_query_volume_tags, winioctl/IOCTL_CHANGER_QUERY_VOLUME_TAGS
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
 - IOCTL_CHANGER_QUERY_VOLUME_TAGS
 - winioctl/IOCTL_CHANGER_QUERY_VOLUME_TAGS
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
 - IOCTL_CHANGER_QUERY_VOLUME_TAGS
---

# IOCTL_CHANGER_QUERY_VOLUME_TAGS IOCTL


## -description

Retrieves the volume tag information for the specified elements.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_CHANGER_QUERY_VOLUME_TAGS,  // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
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

## -see-also

* [CHANGER_SEND_VOLUME_TAG_INFORMATION](ns-winioctl-changer_send_volume_tag_information.md)
* [Device Management Control Codes](/windows/desktop/DevIO/device-management-control-codes)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [READ_ELEMENT_ADDRESS_INFO](ns-winioctl-read_element_address_info.md)