---
UID: NI:winioctl.IOCTL_STORAGE_FIRMWARE_ACTIVATE
title: IOCTL_STORAGE_FIRMWARE_ACTIVATE
author: windows-sdk-content
description: Windows applications can use this control code to activate a firmware image on a specified device.
old-location: fs\ioctl_storage_firmware_activate.htm
old-project: fileio
ms.assetid: 000BEB58-D91E-4859-AC31-A4C72B84A982
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOCTL_STORAGE_FIRMWARE_ACTIVATE, IOCTL_STORAGE_FIRMWARE_ACTIVATE control, IOCTL_STORAGE_FIRMWARE_ACTIVATE control code [Files], fs.ioctl_storage_firmware_activate, winioctl/IOCTL_STORAGE_FIRMWARE_ACTIVATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: WRITE_THROUGH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoctl.h
api_name:
 - IOCTL_STORAGE_FIRMWARE_ACTIVATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_STORAGE_FIRMWARE_ACTIVATE IOCTL


## -description


Windows applications can use this control code to activate a firmware image on a specified device.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
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
                    (DWORD)        IOCTL_STORAGE_FIRMWARE_ACTIVATE, // dwIoControlCode(LPDWORD)      lpInBuffer,      // input buffer
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




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/77E50787-1E71-4D90-A1D3-E6665CE0EFDC">IOCTL_STORAGE_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/DBF40C42-2282-4F0E-B83A-D3154D7EF332">IOCTL_STORAGE_FIRMWARE_GET_INFO</a>



<a href="https://msdn.microsoft.com/2DAAC1FE-2503-4820-9718-9A653B0A05CA">STORAGE_HW_FIRMWARE_ACTIVATE</a>



<a href="https://msdn.microsoft.com/BD1D39C7-9624-400C-BF4D-5F7583AA82FB">STORAGE_HW_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/7BDACD50-0FD1-4F00-BAE5-884D8C1485BC">STORAGE_HW_FIRMWARE_INFO</a>



<a href="https://msdn.microsoft.com/1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1">STORAGE_HW_FIRMWARE_INFO_QUERY</a>



<a href="https://msdn.microsoft.com/37475351-DE0F-4B80-B26B-1482FBCC16CD">STORAGE_HW_FIRMWARE_SLOT_INFO</a>
 

 

