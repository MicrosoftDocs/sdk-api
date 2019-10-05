---
UID: NI:winioctl.IOCTL_STORAGE_MEDIA_REMOVAL
title: IOCTL_STORAGE_MEDIA_REMOVAL
author: windows-sdk-content
description: Enables or disables the mechanism that ejects media, for those devices possessing that locking capability.
old-location: base\ioctl_storage_media_removal.htm
tech.root: devio
ms.assetid: 5971daa1-3bb7-4050-b252-2f5cabb1bf67
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_MEDIA_REMOVAL, IOCTL_STORAGE_MEDIA_REMOVAL control, IOCTL_STORAGE_MEDIA_REMOVAL control code, _win32_ioctl_storage_media_removal, base.ioctl_storage_media_removal, winioctl/IOCTL_STORAGE_MEDIA_REMOVAL
ms.topic: ioctl
f1_keywords:
- winioctl/IOCTL_STORAGE_MEDIA_REMOVAL
dev_langs:
 - c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
- IOCTL_STORAGE_MEDIA_REMOVAL
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_MEDIA_REMOVAL IOCTL


## -description


Enables or disables the mechanism that ejects media, for those devices possessing that locking capability.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_STORAGE_MEDIA_REMOVAL, // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer 
  (DWORD) nInBufferSize,       // size of input buffer 
  NULL,                        // lpOutBuffer0,                           // nOutBufferSize(LPDWORD) lpBytesReturned,   // number of bytes returned
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




## -remarks



The 
<b>IOCTL_STORAGE_MEDIA_REMOVAL</b> control code is valid only for devices that support removable media.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_eject_media">IOCTL_STORAGE_EJECT_MEDIA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_load_media">IOCTL_STORAGE_LOAD_MEDIA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-prevent_media_removal">PREVENT_MEDIA_REMOVAL</a>
 

 

