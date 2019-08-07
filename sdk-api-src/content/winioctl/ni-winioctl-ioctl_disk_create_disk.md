---
UID: NI:winioctl.IOCTL_DISK_CREATE_DISK
title: IOCTL_DISK_CREATE_DISK
author: windows-sdk-content
description: Initializes the specified disk and disk partition table using the information in the CREATE_DISK structure.
old-location: fs\ioctl_disk_create_disk.htm
tech.root: FileIO
ms.assetid: c8215a00-ea39-4268-bb66-68cf3d37baef
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_CREATE_DISK, IOCTL_DISK_CREATE_DISK control, IOCTL_DISK_CREATE_DISK control code [Files], _win32_ioctl_disk_create_disk, base.ioctl_disk_create_disk, fs.ioctl_disk_create_disk, winioctl/IOCTL_DISK_CREATE_DISK
ms.topic: ioctl
f1_keywords:
- winioctl/IOCTL_DISK_CREATE_DISK
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
- IOCTL_DISK_CREATE_DISK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_CREATE_DISK IOCTL


## -description


Initializes the specified disk and disk partition table using the information in the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-create_disk">CREATE_DISK</a> structure.

To perform this operation, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following 
    parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl( (HANDLE) hDevice,              // handle to device
                      IOCTL_DISK_CREATE_DISK,        // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
                      (DWORD) nInBufferSize,         // size of input buffer
                      (LPVOID) NULL,                 // lpOutBuffer(DWORD) 0,                     // nOutBufferSize(LPDWORD) lpBytesReturned,     // number of bytes returned
                      (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure</pre>
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



When specifying a GUID partition table (GPT) as the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-partition_style">PARTITION_STYLE</a> of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-create_disk">CREATE_DISK</a> structure, an application should wait for the 
    MSR partition arrival before sending the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout_ex">IOCTL_DISK_SET_DRIVE_LAYOUT_EX</a> control code. 
    For more information about device notification, see 
    <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-create_disk">CREATE_DISK</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>
 

 

