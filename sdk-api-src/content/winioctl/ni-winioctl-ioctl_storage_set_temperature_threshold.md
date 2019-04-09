---
UID: NI:winioctl.IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
title: IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD (winioctl.h)
author: windows-sdk-content
description: Windows applications can use this control code to set the temperature threshold of a device (when it's supported by the device).
old-location: fs\ioctl_storage_set_temperature_threshold.htm
tech.root: FileIO
ms.assetid: 6B4BF202-6CC9-4571-9078-019984805F00
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD, IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD control, IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD control code [Files], fs.ioctl_storage_set_temperature_threshold, winioctl/IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
ms.topic: ioctl
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
 - IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD IOCTL


## -description


Windows applications can use this control code to set the temperature threshold of a device (when it's supported by the device).  Use <a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a> to determine if the device supports changing the over and under temperature thresholds.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
   function with the following parameters.

```cpp
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                    (DWORD)        IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD, // dwIoControlCode(LPDWORD)      lpInBuffer,      // input buffer
                    (DWORD)        nInBufferSize,   // size of input buffer
                    (LPDWORD)      lpOutBuffer,     // output buffer
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



<a href="https://msdn.microsoft.com/6755dcd4-e4a0-423f-9dcc-b9719c8e5c88">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://msdn.microsoft.com/9747be01-7c70-4697-97f7-e3830b54ba0a">STORAGE_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>



<a href="https://msdn.microsoft.com/236B4AC7-AF5E-4556-9FFD-D64C450E6492">STORAGE_TEMPERATURE_INFO</a>



<a href="https://msdn.microsoft.com/02E01EAE-FF0F-4013-A237-651B1428DF52">STORAGE_TEMPERATURE_THRESHOLD</a>
 

 

