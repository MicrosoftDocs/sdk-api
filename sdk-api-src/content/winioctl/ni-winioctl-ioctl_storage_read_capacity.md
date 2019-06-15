---
UID: NI:winioctl.IOCTL_STORAGE_READ_CAPACITY
title: IOCTL_STORAGE_READ_CAPACITY
author: windows-sdk-content
description: Retrieves the geometry information for the device.
old-location: base\ioctl_storage_read_capacity.htm
tech.root: devio
ms.assetid: c0a2c73c-fae9-40e9-8009-4dffbb03a01d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_READ_CAPACITY, IOCTL_STORAGE_READ_CAPACITY control, IOCTL_STORAGE_READ_CAPACITY control code, base.ioctl_storage_read_capacity, winioctl/IOCTL_STORAGE_READ_CAPACITY
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1
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
 - IOCTL_STORAGE_READ_CAPACITY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_READ_CAPACITY IOCTL


## -description


Retrieves the geometry information for the device.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
 (HANDLE) hDevice,            // handle to device 
 IOCTL_STORAGE_READ_CAPACITY, // dwIoControlCodeNULL,                        // lpInBuffer0,                           // nInBufferSize(LPVOID) lpOutBuffer,        // output buffer 
 (DWORD) nOutBufferSize,      // size of output buffer 
 (LPDWORD) lpBytesReturned,   // number of bytes returned 
 (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure 
);</pre>
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




<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/storage-read-capacity">STORAGE_READ_CAPACITY</a>
 

 

