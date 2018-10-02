---
UID: NI:winioctl.IOCTL_CHANGER_QUERY_VOLUME_TAGS
title: IOCTL_CHANGER_QUERY_VOLUME_TAGS
author: windows-sdk-content
description: Retrieves the volume tag information for the specified elements.
old-location: base\ioctl_changer_query_volume_tags.htm
tech.root: devio
ms.assetid: 67c440e1-cef8-459d-b811-0b483ff51e7e
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IOCTL_CHANGER_QUERY_VOLUME_TAGS, IOCTL_CHANGER_QUERY_VOLUME_TAGS control, IOCTL_CHANGER_QUERY_VOLUME_TAGS control code, _win32_ioctl_changer_query_volume_tags, base.ioctl_changer_query_volume_tags, winioctl/IOCTL_CHANGER_QUERY_VOLUME_TAGS
ms.prod: windows
ms.technology: windows-sdk
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
 - IOCTL_CHANGER_QUERY_VOLUME_TAGS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_CHANGER_QUERY_VOLUME_TAGS IOCTL


## -description


Retrieves the volume tag information for the specified elements.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_CHANGER_QUERY_VOLUME_TAGS, // dwIoControlCode(LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
  (LPVOID) lpOutBuffer,            // output buffer
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




## -see-also




<a href="https://msdn.microsoft.com/96148983-48be-466d-be7f-c1dbf6910c20">CHANGER_SEND_VOLUME_TAG_INFORMATION</a>



<a href="https://msdn.microsoft.com/b3a3ffa1-e710-4d96-aff8-5b6876ab032b">Device Management Control Codes</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/2b7e611b-7db6-4ba6-ae1f-4269a96dbb16">READ_ELEMENT_ADDRESS_INFO</a>
 

 

