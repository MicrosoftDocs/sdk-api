---
UID: NI:winioctl.IOCTL_DISK_GET_DRIVE_LAYOUT
title: IOCTL_DISK_GET_DRIVE_LAYOUT
author: windows-driver-content
description: Retrieves information for each entry in the partition tables for a disk.
old-location: fs\ioctl_disk_get_drive_layout.htm
old-project: FileIO
ms.assetid: 6c1bc445-3cd1-4f86-a36b-f74ad8f4d2e5
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_LAYOUT, IOCTL_DISK_GET_DRIVE_LAYOUT control, IOCTL_DISK_GET_DRIVE_LAYOUT control code [Files], _win32_ioctl_disk_get_drive_layout, base.ioctl_disk_get_drive_layout, fs.ioctl_disk_get_drive_layout, winioctl/IOCTL_DISK_GET_DRIVE_LAYOUT
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
-	IOCTL_DISK_GET_DRIVE_LAYOUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_DISK_GET_DRIVE_LAYOUT IOCTL


## -description


Retrieves information for each entry in the  partition tables for a disk.
<div class="alert"><b>Note</b>  <b>IOCTL_DISK_GET_DRIVE_LAYOUT</b> has been superseded by 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560364">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>, which retrieves layout information for AT and EFI (Extensible Firmware Interface) partitions.</div><div> </div>To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters. You must have read access to the drive in order to use this control code.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_DISK_GET_DRIVE_LAYOUT, // dwIoControlCode
  NULL,                        // lpInBuffer
  0,                           // nInBufferSize
  (LPVOID) lpOutBuffer,        // output buffer
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




## -remarks



This operation retrieves information for each primary partition as well as each logical drive. To determine whether the entry is an extended or unused partition, check the <a href="https://msdn.microsoft.com/b2e15b93-a02b-4d6f-b242-b5ec9a30c97b">disk partition type</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552659">DRIVE_LAYOUT_INFORMATION</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560364">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff560408">IOCTL_DISK_SET_DRIVE_LAYOUT</a>
 

 

