---
UID: NI:winioctl.IOCTL_DISK_GET_DRIVE_GEOMETRY
title: IOCTL_DISK_GET_DRIVE_GEOMETRY
author: windows-sdk-content
description: Retrieves information about the physical disk's geometry:\_type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.
old-location: fs\ioctl_disk_get_drive_geometry.htm
old-project: FileIO
ms.assetid: 574efc29-112b-42fe-ad1b-72543f20e831
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_GEOMETRY, IOCTL_DISK_GET_DRIVE_GEOMETRY control, IOCTL_DISK_GET_DRIVE_GEOMETRY control code [Files], _win32_ioctl_disk_get_drive_geometry, base.ioctl_disk_get_drive_geometry, fs.ioctl_disk_get_drive_geometry, winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_DISK_GET_DRIVE_GEOMETRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_DISK_GET_DRIVE_GEOMETRY IOCTL


## -description


Retrieves information about the physical disk's geometry: type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.
<div class="alert"><b>Note</b>  <b>IOCTL_DISK_GET_DRIVE_GEOMETRY</b> has been superseded by 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560359">IOCTL_DISK_GET_DRIVE_GEOMETRY_EX</a>, which retrieves additional information.</div><div> </div>To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552613">DISK_GEOMETRY</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560359">IOCTL_DISK_GET_DRIVE_GEOMETRY_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560559">IOCTL_STORAGE_GET_MEDIA_TYPES</a>
 

 

