---
UID: NI:winioctl.IOCTL_DISK_GET_DRIVE_LAYOUT_EX
title: IOCTL_DISK_GET_DRIVE_LAYOUT_EX
author: windows-sdk-content
description: Retrieves extended information for each entry in the partition tables for a disk.
old-location: fs\ioctl_disk_get_drive_layout_ex.htm
tech.root: FileIO
ms.assetid: 21507182-5a33-4e58-b5ed-3724feefa4ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_DRIVE_LAYOUT_EX, IOCTL_DISK_GET_DRIVE_LAYOUT_EX control, IOCTL_DISK_GET_DRIVE_LAYOUT_EX control code [Files], _win32_ioctl_disk_get_drive_layout_ex, base.ioctl_disk_get_drive_layout_ex, fs.ioctl_disk_get_drive_layout_ex, winioctl/IOCTL_DISK_GET_DRIVE_LAYOUT_EX
ms.topic: ioctl
f1_keywords:
- winioctl/IOCTL_DISK_GET_DRIVE_LAYOUT_EX
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
- IOCTL_DISK_GET_DRIVE_LAYOUT_EX
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GET_DRIVE_LAYOUT_EX IOCTL


## -description


Retrieves extended information for each entry in the  partition tables for a disk.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl( (HANDLE) hDevice,               // handle to device
                      IOCTL_DISK_GET_DRIVE_LAYOUT_EX, // dwIoControlCode
                      NULL,                           // lpInBuffer
                      0,                              // nInBufferSize
                      (LPVOID) lpOutBuffer,           // output buffer
                      (DWORD) nOutBufferSize,         // size of output buffer
                      (LPDWORD) lpBytesReturned,      // number of bytes returned
                      (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
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



This operation retrieves information for each primary partition as well as each logical drive. To determine 
     whether the entry is an extended or unused partition, check the 
     <a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-partition-types">disk partition type</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information_ex">DRIVE_LAYOUT_INFORMATION_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout_ex">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a>
 

 

