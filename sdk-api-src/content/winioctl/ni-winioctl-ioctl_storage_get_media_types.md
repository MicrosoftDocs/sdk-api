---
UID: NI:winioctl.IOCTL_STORAGE_GET_MEDIA_TYPES
title: IOCTL_STORAGE_GET_MEDIA_TYPES (winioctl.h)
author: windows-sdk-content
description: Retrieves the geometry information for the device.
old-location: base\ioctl_storage_get_media_types.htm
tech.root: devio
ms.assetid: 67f65549-f24b-4ef2-a98f-1fc618a3bb77
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_GET_MEDIA_TYPES, IOCTL_STORAGE_GET_MEDIA_TYPES control, IOCTL_STORAGE_GET_MEDIA_TYPES control code, _win32_ioctl_storage_get_media_types, base.ioctl_storage_get_media_types, winioctl/IOCTL_STORAGE_GET_MEDIA_TYPES
ms.topic: ioctl
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_STORAGE_GET_MEDIA_TYPES
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOCTL_STORAGE_GET_MEDIA_TYPES IOCTL


## -description


Retrieves the geometry information for the device.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_STORAGE_GET_MEDIA_TYPES,   // dwIoControlCodeNULL,                            // lpInBuffer0,                               // nInBufferSize(LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## -ioctlparameters




### -input-buffer



<text></text>




### -input-buffer-length



<text></text>




### -output-buffer



<text></text>




### -output-buffer-length



<text></text>




### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block



Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



This device I/O control operation is for all class drivers, as well as non-SCSI hard drives and floppy disk devices.




## -see-also




<a href="https://msdn.microsoft.com/5e5955b4-1319-42c9-9df8-9910c05dec69">DISK_GEOMETRY</a>



<a href="https://msdn.microsoft.com/b3a3ffa1-e710-4d96-aff8-5b6876ab032b">Device Management Control Codes</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/574efc29-112b-42fe-ad1b-72543f20e831">IOCTL_DISK_GET_DRIVE_GEOMETRY</a>
 

 

