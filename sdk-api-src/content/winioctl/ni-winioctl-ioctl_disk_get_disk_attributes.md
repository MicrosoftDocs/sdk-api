---
UID: NI:winioctl.IOCTL_DISK_GET_DISK_ATTRIBUTES
title: IOCTL_DISK_GET_DISK_ATTRIBUTES
author: windows-sdk-content
description: Retrieves the attributes of the specified disk device.
old-location: fs\ioctl_disk_get_disk_attributes.htm
tech.root: fileio
ms.assetid: 3fa9fabb-91ef-4306-90b6-c3dd17f3e298
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOCTL_DISK_GET_DISK_ATTRIBUTES, IOCTL_DISK_GET_DISK_ATTRIBUTES control, IOCTL_DISK_GET_DISK_ATTRIBUTES control code [Files], fs.ioctl_disk_get_disk_attributes, winioctl/IOCTL_DISK_GET_DISK_ATTRIBUTES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IOCTL_DISK_GET_DISK_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GET_DISK_ATTRIBUTES IOCTL


## -description


Retrieves the attributes of the specified disk device.

To perform this operation, call the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following 
    parameters.

```cpp
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_GET_DISK_ATTRIBUTES, // dwIoControlCode(LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
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




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/c6a0461d-cc23-4191-a0ff-c4279c1b097e">GET_DISK_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/ba0e3666-8660-493c-b821-5997d577e7e2">IOCTL_DISK_SET_DISK_ATTRIBUTES</a>
 

 

