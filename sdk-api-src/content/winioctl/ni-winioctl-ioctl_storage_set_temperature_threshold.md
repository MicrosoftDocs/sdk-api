---
UID: NI:winioctl.IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
title: IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
author: windows-sdk-content
description: Windows applications can use this control code to set the temperature threshold of a device (when it's supported by the device).
old-location: fs\ioctl_storage_set_temperature_threshold.htm
tech.root: FileIO
ms.assetid: 6B4BF202-6CC9-4571-9078-019984805F00
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD, IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD control, IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD control code [Files], fs.ioctl_storage_set_temperature_threshold, winioctl/IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD
ms.topic: ioctl
f1_keywords: ["winioctl/IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD"]
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


Windows applications can use this control code to set the temperature threshold of a device (when it's supported by the device).  Use <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a> to determine if the device supports changing the over and under temperature thresholds.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                    (DWORD)        IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD, // dwIoControlCode(LPDWORD)      lpInBuffer,      // input buffer
                    (DWORD)        nInBufferSize,   // size of input buffer
                    (LPDWORD)      lpOutBuffer,     // output buffer
                    (DWORD)        nOutBufferSize,  // size of output buffer
                    (LPDWORD)      lpBytesReturned, // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
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




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_query_property">IOCTL_STORAGE_QUERY_PROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-_storage_property_id">STORAGE_PROPERTY_ID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_property_query">STORAGE_PROPERTY_QUERY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_temperature_info">STORAGE_TEMPERATURE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_storage_temperature_threshold">STORAGE_TEMPERATURE_THRESHOLD</a>
 

 

