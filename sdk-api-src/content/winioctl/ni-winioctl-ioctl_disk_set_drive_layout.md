---
UID: NI:winioctl.IOCTL_DISK_SET_DRIVE_LAYOUT
title: IOCTL_DISK_SET_DRIVE_LAYOUT
author: windows-sdk-content
description: Partitions a disk as specified by drive layout and partition information data.
old-location: fs\ioctl_disk_set_drive_layout.htm
tech.root: FileIO
ms.assetid: 8cace6a5-666a-4d35-a557-6bf0564dbe58
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_SET_DRIVE_LAYOUT, IOCTL_DISK_SET_DRIVE_LAYOUT control, IOCTL_DISK_SET_DRIVE_LAYOUT control code [Files], _win32_ioctl_disk_set_drive_layout, base.ioctl_disk_set_drive_layout, fs.ioctl_disk_set_drive_layout, winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT
ms.topic: ioctl
f1_keywords: 
 - "winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT"
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
 - IOCTL_DISK_SET_DRIVE_LAYOUT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_SET_DRIVE_LAYOUT IOCTL


## -description


Partitions a disk as specified by drive layout and partition information data.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the parameters specified below.

<b>IOCTL_DISK_SET_DRIVE_LAYOUT</b> has been superseded by 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout_ex">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a>, which retrieves layout information for AT and EFI (Extensible Firmware Interface) partitions.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_DISK_SET_DRIVE_LAYOUT, // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer 
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



If the partition is on a disk formatted as type master boot record (MBR), partition size totals cannot exceed 2 TB per MBR disk. For example, a disk of type MBR can have a single 2-TB partition, two 1-TB partitions, or any combination that does not total more than 2 TB. If more space is required, a disk formatted as type GUID partition table (GPT) should be used. If third-party partitioning tools are used  to work around this limitation on disks of type MBR larger than 2 TB, configuration operations via the disk partitioning IOCTL control codes will be limited.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_drive_layout_information">DRIVE_LAYOUT_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk
		  Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout_ex">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout_ex">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a>
 

 

