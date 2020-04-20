---
UID: NI:winioctl.IOCTL_DISK_DELETE_DRIVE_LAYOUT
title: IOCTL_DISK_DELETE_DRIVE_LAYOUT
description: Removes the boot signature from the master boot record, so that the disk will be formatted from sector zero to the end of the disk.helpviewer_keywords: ["IOCTL_DISK_DELETE_DRIVE_LAYOUT","IOCTL_DISK_DELETE_DRIVE_LAYOUT control","IOCTL_DISK_DELETE_DRIVE_LAYOUT control code [Files]","base.ioctl_disk_delete_drive_layout","fs.ioctl_disk_delete_drive_layout","winioctl/IOCTL_DISK_DELETE_DRIVE_LAYOUT"]
old-location: fs\ioctl_disk_delete_drive_layout.htm
tech.root: FileIO
ms.assetid: b790e1f8-9371-4ff9-a820-3ea1af29cc6b
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_DELETE_DRIVE_LAYOUT, IOCTL_DISK_DELETE_DRIVE_LAYOUT control, IOCTL_DISK_DELETE_DRIVE_LAYOUT control code [Files], base.ioctl_disk_delete_drive_layout, fs.ioctl_disk_delete_drive_layout, winioctl/IOCTL_DISK_DELETE_DRIVE_LAYOUT
f1_keywords:
- winioctl/IOCTL_DISK_DELETE_DRIVE_LAYOUT
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
- IOCTL_DISK_DELETE_DRIVE_LAYOUT
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_DELETE_DRIVE_LAYOUT IOCTL


## -description


Removes the boot signature from the master boot record, so that the disk will be formatted from sector zero to the end of the disk. Partition information is no longer stored in sector zero.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,               // handle to device
  IOCTL_DISK_DELETE_DRIVE_LAYOUT, // dwIoControlCodeNULL,                           // lpInBuffer0,                              // nInBufferSizeNULL,                           // lpOutBuffer0,                              // nOutBufferSize(LPDWORD) lpBytesReturned,      // number of bytes returned
  (LPOVERLAPPED) lpOverlapped     // OVERLAPPED structure
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




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk
    Management Control Codes</a>
 

 

