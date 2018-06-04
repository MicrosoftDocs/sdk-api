---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOCTL_STORAGE_QUERY_PROPERTY IOCTL


## -description


Windows applications can use this control code to return the properties of a storage device or adapter. The request indicates the kind of information 
    to retrieve, such as the inquiry data for a device or the capabilities and limitations of an adapter. 
    <b>IOCTL_STORAGE_QUERY_PROPERTY</b> can also be used 
    to determine whether the port driver supports a particular property or which fields in the property descriptor can 
    be modified with a subsequent change-property request.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl(
     _In_        (HANDLE)       hDevice,               // handle to a partition
     _In_        (DWORD) IOCTL_STORAGE_QUERY_PROPERTY, // dwIoControlCode
     _In_        (LPVOID)       lpInBuffer,            // input buffer - STORAGE_PROPERTY_QUERY structure
     _In_        (DWORD)        nInBufferSize,         // size of input buffer
     _Out_opt_   (LPVOID)       lpOutBuffer,           // output buffer - see Remarks
     _In_        (DWORD)        nOutBufferSize,        // size of output buffer
     _Out_opt_   (LPDWORD)      lpBytesReturned,       // number of bytes returned
     _Inout_opt_ (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure</pre>
</td>
</tr>
</table></span></div>

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
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff566997">STORAGE_PROPERTY_QUERY</a> structure pointed to by the 
     <i>lpInBuffer</i> parameter. These values are enumerated by the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff566996">STORAGE_PROPERTY_ID</a> enumeration. If the 
     <b>QueryType</b> member of the 
     <b>STORAGE_PROPERTY_QUERY</b> is set to 
     <b>PropertyExistsQuery</b> then no structure is returned.




## -see-also




<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566968">STORAGE_DESCRIPTOR_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566997">STORAGE_PROPERTY_QUERY</a>
 

 

