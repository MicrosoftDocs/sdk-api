---
UID: NI:winioctl.IOCTL_STORAGE_QUERY_PROPERTY
title: IOCTL_STORAGE_QUERY_PROPERTY (winioctl.h)
author: windows-sdk-content
description: Windows applications can use this control code to return the properties of a storage device or adapter.
old-location: fs\ioctl_storage_query_property.htm
tech.root: FileIO
ms.assetid: 6755dcd4-e4a0-423f-9dcc-b9719c8e5c88
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_QUERY_PROPERTY, IOCTL_STORAGE_QUERY_PROPERTY control, IOCTL_STORAGE_QUERY_PROPERTY control code [Files], fs.ioctl_storage_query_property, winioctl/IOCTL_STORAGE_QUERY_PROPERTY
ms.topic: ioctl
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_STORAGE_QUERY_PROPERTY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_QUERY_PROPERTY IOCTL


## -description


Windows applications can use this control code to return the properties of a storage device or adapter. The request indicates the kind of information 
    to retrieve, such as the inquiry data for a device or the capabilities and limitations of an adapter. 
    <b>IOCTL_STORAGE_QUERY_PROPERTY</b> can also be used 
    to determine whether the port driver supports a particular property or which fields in the property descriptor can 
    be modified with a subsequent change-property request.

```cpp
BOOL 
WINAPI 
DeviceIoControl(
     _In_        (HANDLE)       hDevice,               // handle to a partition
     _In_        (DWORD) IOCTL_STORAGE_QUERY_PROPERTY, // dwIoControlCode
     _In_        (LPVOID)       lpInBuffer,            // input buffer - STORAGE_PROPERTY_QUERY structure
     _In_        (DWORD)        nInBufferSize,         // size of input buffer
     _Out_opt_   (LPVOID)       lpOutBuffer,           // output buffer - see Remarks
     _In_        (DWORD)        nOutBufferSize,        // size of output buffer
     _Out_opt_   (LPDWORD)      lpBytesReturned,       // number of bytes returned
     _Inout_opt_ (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
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



The optional output buffer returned through the <i>lpOutBuffer</i> parameter can be one of 
     several structures depending on the value of the <b>PropertyId</b> member of the 
     <a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a> structure pointed to by the 
     <i>lpInBuffer</i> parameter. These values are enumerated by the 
     <a href="https://msdn.microsoft.com/9747be01-7c70-4697-97f7-e3830b54ba0a">STORAGE_PROPERTY_ID</a> enumeration. If the 
     <b>QueryType</b> member of the 
     <b>STORAGE_PROPERTY_QUERY</b> is set to 
     <b>PropertyExistsQuery</b> then no structure is returned.




## -see-also




<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/f98e53d5-45cb-4c3f-b04d-8eecd98655d2">STORAGE_DESCRIPTOR_HEADER</a>



<a href="https://msdn.microsoft.com/c97a14ab-628c-41f1-96c3-0f47654d0606">STORAGE_PROPERTY_QUERY</a>
 

 

