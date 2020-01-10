---
UID: NI:winioctl.IOCTL_DISK_GET_CACHE_INFORMATION
title: IOCTL_DISK_GET_CACHE_INFORMATION
description: Retrieves the disk cache configuration data.
old-location: fs\ioctl_disk_get_cache_information.htm
tech.root: FileIO
ms.assetid: 025a92e8-6169-4d7e-9029-f22acb2bdc9f
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_CACHE_INFORMATION, IOCTL_DISK_GET_CACHE_INFORMATION control, IOCTL_DISK_GET_CACHE_INFORMATION control code [Files], base.ioctl_disk_get_cache_information, fs.ioctl_disk_get_cache_information, winioctl/IOCTL_DISK_GET_CACHE_INFORMATION
f1_keywords:
- winioctl/IOCTL_DISK_GET_CACHE_INFORMATION
dev_langs:
- c++
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
- IOCTL_DISK_GET_CACHE_INFORMATION
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GET_CACHE_INFORMATION IOCTL


## -description


Retrieves the disk cache configuration data.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_GET_CACHE_INFORMATION, // dwIoControlCodeNULL,                             // lpInBuffer0,                                // nInBufferSize(LPVOID) lpOutBuffer,             // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
  (LPDWORD) lpBytesReturned,        // number of bytes returned
  (LPOVERLAPPED) lpOverlapped       // OVERLAPPED structure
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




## -remarks



To set the disk cache information, use the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_cache_information">IOCTL_DISK_SET_CACHE_INFORMATION</a> control code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-disk_cache_information">DISK_CACHE_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_cache_information">IOCTL_DISK_SET_CACHE_INFORMATION</a>
 

 

