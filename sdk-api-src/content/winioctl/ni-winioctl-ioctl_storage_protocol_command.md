---
UID: NI:winioctl.IOCTL_STORAGE_PROTOCOL_COMMAND
title: IOCTL_STORAGE_PROTOCOL_COMMAND
author: windows-sdk-content
description: Windows applications can use this control code to return properties of a storage device or adapter. The request indicates the kind of information to retrieve, such as inquiry data for a device or capabilities and limitations of an adapter.
old-location: fs\ioctl_storage_protocol_command.htm
tech.root: fileio
ms.assetid: 77027740-CDFD-422A-B458-C36B2E346EFD
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IOCTL_STORAGE_PROTOCOL_COMMAND, IOCTL_STORAGE_PROTOCOL_COMMAND control, IOCTL_STORAGE_PROTOCOL_COMMAND control code [Files], fs.ioctl_storage_protocol_command, winioctl/IOCTL_STORAGE_PROTOCOL_COMMAND
ms.prod: windows
ms.technology: windows-sdk
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
 - winioctl.h
api_name:
 - IOCTL_STORAGE_QUERY_PROPERTY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_PROTOCOL_COMMAND IOCTL


## -description


Windows applications can use this control code to return properties of a storage device or adapter. The request indicates the kind of information to retrieve, such as inquiry data for a device or capabilities and limitations of an adapter.
     
    

<b>IOCTL_STORAGE_QUERY_PROPERTY</b> can also be used to determine whether the port driver supports a particular property or which fields in the property descriptor can be modified with a subsequent change-property request. 

Usually, the caller is a storage class driver, but the caller can be an application that makes requests directly to the port driver when no storage class driver exists for the target device.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
   function with the following parameters.

```cpp
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                    (DWORD)        IOCTL_STORAGE_QUERY_PROPERTY, // dwIoControlCode(LPDWORD)      lpInBuffer,      // input buffer
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



<a href="https://msdn.microsoft.com/9747be01-7c70-4697-97f7-e3830b54ba0a">STORAGE_PROPERTY_ID</a>



<a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>
 

 

