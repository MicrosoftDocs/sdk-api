---
UID: NI:winioctl.IOCTL_STORAGE_FIRMWARE_GET_INFO
title: IOCTL_STORAGE_FIRMWARE_GET_INFO
author: windows-sdk-content
description: Windows applications can use this control code to query the storage device for detailed firmware information.
old-location: fs\ioctl_storage_firmware_get_info.htm
old-project: fileio
ms.assetid: DBF40C42-2282-4F0E-B83A-D3154D7EF332
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOCTL_STORAGE_FIRMWARE_GET_INFO, IOCTL_STORAGE_FIRMWARE_GET_INFO control, IOCTL_STORAGE_FIRMWARE_GET_INFO control code [Files], fs.ioctl_storage_firmware_get_info, winioctl/IOCTL_STORAGE_FIRMWARE_GET_INFO
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
tech.root: 
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoctl.h
api_name:
 - IOCTL_STORAGE_FIRMWARE_GET_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_STORAGE_FIRMWARE_GET_INFO IOCTL


## -description


Windows applications can use this control code to query the storage device for detailed firmware information. A successful call will return information about firmware revisions, activity status, as well as read/write attributes for each slot. The amount of data returned will vary based on storage protocol.

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
                    (DWORD)        IOCTL_STORAGE_FIRMWARE_GET_INFO, // dwIoControlCode(LPDWORD)      lpInBuffer,      // input buffer
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



<a href="https://msdn.microsoft.com/library/windows/hardware/dn932065">IOCTL_STORAGE_FIRMWARE_ACTIVATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn932066">IOCTL_STORAGE_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931808">STORAGE_HW_FIRMWARE_ACTIVATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931809">STORAGE_HW_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931810">STORAGE_HW_FIRMWARE_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931811">STORAGE_HW_FIRMWARE_INFO_QUERY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931812">STORAGE_HW_FIRMWARE_SLOT_INFO</a>
 

 

