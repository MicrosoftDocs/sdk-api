---
UID: NI:winioctl.IOCTL_DISK_GET_DRIVE_GEOMETRY
title: IOCTL_DISK_GET_DRIVE_GEOMETRY
description: Retrieves information about the physical disk's geometry:\_type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.
old-location: fs\ioctl_disk_get_drive_geometry.htm
tech.root: FileIO
ms.assetid: 574efc29-112b-42fe-ad1b-72543f20e831
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_GEOMETRY, IOCTL_DISK_GET_DRIVE_GEOMETRY control, IOCTL_DISK_GET_DRIVE_GEOMETRY control code [Files], _win32_ioctl_disk_get_drive_geometry, base.ioctl_disk_get_drive_geometry, fs.ioctl_disk_get_drive_geometry, winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY
f1_keywords:
- winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY
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
- IOCTL_DISK_GET_DRIVE_GEOMETRY
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GET_DRIVE_GEOMETRY IOCTL


## -description


Retrieves information about the physical disk's geometry: type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.
<div class="alert"><b>Note</b>  <b>IOCTL_DISK_GET_DRIVE_GEOMETRY</b> has been superseded by 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry_ex">IOCTL_DISK_GET_DRIVE_GEOMETRY_EX</a>, which retrieves additional information.</div><div> </div>To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to device
  IOCTL_DISK_GET_DRIVE_GEOMETRY, // dwIoControlCodeNULL,                          // lpInBuffer0,                             // nInBufferSize(LPVOID) lpOutBuffer,          // output buffer
  (DWORD) nOutBufferSize,        // size of output buffer
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-disk_geometry">DISK_GEOMETRY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_geometry_ex">IOCTL_DISK_GET_DRIVE_GEOMETRY_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_media_types">IOCTL_STORAGE_GET_MEDIA_TYPES</a>
 

 

