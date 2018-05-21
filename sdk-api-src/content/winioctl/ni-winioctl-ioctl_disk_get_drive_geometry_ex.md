---
UID: NI:winioctl.IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
title: IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
author: windows-driver-content
description: Retrieves extended information about the physical disk's geometry:\_type, number of cylinders, tracks per cylinder, sectors per track, and bytes per sector.
old-location: fs\ioctl_disk_get_drive_geometry_ex.htm
old-project: FileIO
ms.assetid: 8a0667c8-b182-4851-af8e-411d95da0e3b
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_GEOMETRY_EX, IOCTL_DISK_GET_DRIVE_GEOMETRY_EX control, IOCTL_DISK_GET_DRIVE_GEOMETRY_EX control code [Files], _win32_ioctl_disk_get_drive_geometry_ex, base.ioctl_disk_get_drive_geometry_ex, fs.ioctl_disk_get_drive_geometry_ex, winioctl/IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	IOCTL_DISK_GET_DRIVE_GEOMETRY_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
<pre>
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to volume
  IOCTL_DISK_GET_DRIVE_GEOMETRY_EX, // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  (LPVOID) lpOutBuffer,             // output buffer
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



When specifying a GUID partition table (GPT) as the <a href="https://msdn.microsoft.com/library/windows/hardware/ff563773">PARTITION_STYLE</a> of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552484">CREATE_DISK</a> structure, an application should wait for the MSR partition arrival before sending the <a href="https://msdn.microsoft.com/library/windows/hardware/ff560411">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a> control code. For more information about device notification, see <a href="https://msdn.microsoft.com/82094d95-9af3-4222-9c5e-ce2df9bab5e3">RegisterDeviceNotification</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552618">DISK_GEOMETRY_EX</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>
 

 

