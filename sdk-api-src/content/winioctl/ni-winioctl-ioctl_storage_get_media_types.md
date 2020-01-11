---
UID: NI:winioctl.IOCTL_STORAGE_GET_MEDIA_TYPES
title: IOCTL_STORAGE_GET_MEDIA_TYPES
description: Retrieves the geometry information for the device.
old-location: base\ioctl_storage_get_media_types.htm
tech.root: devio
ms.assetid: 67f65549-f24b-4ef2-a98f-1fc618a3bb77
ms.date: 12/05/2018
ms.keywords: IOCTL_STORAGE_GET_MEDIA_TYPES, IOCTL_STORAGE_GET_MEDIA_TYPES control, IOCTL_STORAGE_GET_MEDIA_TYPES control code, _win32_ioctl_storage_get_media_types, base.ioctl_storage_get_media_types, winioctl/IOCTL_STORAGE_GET_MEDIA_TYPES
f1_keywords:
- winioctl/IOCTL_STORAGE_GET_MEDIA_TYPES
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
- IOCTL_STORAGE_GET_MEDIA_TYPES
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_STORAGE_GET_MEDIA_TYPES IOCTL


## -description


Retrieves the geometry information for the device.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_STORAGE_GET_MEDIA_TYPES,   // dwIoControlCodeNULL,                            // lpInBuffer0,                               // nInBufferSize(LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
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



This device I/O control operation is for all class drivers, as well as non-SCSI hard drives and floppy disk devices.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-disk_geometry">DISK_GEOMETRY</a>



<a href="https://docs.microsoft.com/windows/desktop/DevIO/device-management-control-codes">Device Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry">IOCTL_DISK_GET_DRIVE_GEOMETRY</a>
 

 

