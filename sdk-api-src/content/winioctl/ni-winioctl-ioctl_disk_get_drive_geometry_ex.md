---
UID: NI:winioctl.IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
title: IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
description: Retrieves extended information about the physical disk's geometry:\_type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.
old-location: fs\ioctl_disk_get_drive_geometry_ex.htm
tech.root: FileIO
ms.assetid: 8a0667c8-b182-4851-af8e-411d95da0e3b
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_GEOMETRY_EX, IOCTL_DISK_GET_DRIVE_GEOMETRY_EX control, IOCTL_DISK_GET_DRIVE_GEOMETRY_EX control code [Files], _win32_ioctl_disk_get_drive_geometry_ex, base.ioctl_disk_get_drive_geometry_ex, fs.ioctl_disk_get_drive_geometry_ex, winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
f1_keywords:
- winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
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
- IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GET_DRIVE_GEOMETRY_EX IOCTL


## -description


Retrieves extended information about the physical disk's geometry: type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to volume
  IOCTL_DISK_GET_DRIVE_GEOMETRY_EX, // dwIoControlCodeNULL,                             // lpInBuffer0,                                // nInBufferSize(LPVOID) lpOutBuffer,             // output buffer
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



When specifying a GUID partition table (GPT) as the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-partition_style">PARTITION_STYLE</a> of the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-create_disk">CREATE_DISK</a> structure, an application should wait for the MSR partition arrival before sending the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout_ex">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a> control code. For more information about device notification, see <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-disk_geometry_ex">DISK_GEOMETRY_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>
 

 

