---
UID: NI:winioctl.IOCTL_DISK_SET_DRIVE_LAYOUT_EX
title: IOCTL_DISK_SET_DRIVE_LAYOUT_EX
description: Partitions a disk according to the specified drive layout and partition information data.
old-location: fs\ioctl_disk_set_drive_layout_ex.htm
tech.root: FileIO
ms.assetid: a600e841-c692-4aa4-bea2-a33931d9b007
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_SET_DRIVE_LAYOUT_EX, IOCTL_DISK_SET_DRIVE_LAYOUT_EX control, IOCTL_DISK_SET_DRIVE_LAYOUT_EX control code [Files], _win32_ioctl_disk_set_drive_layout_ex, base.ioctl_disk_set_drive_layout_ex, fs.ioctl_disk_set_drive_layout_ex, winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT_EX
ms.topic: ioctl
f1_keywords:
- winioctl/IOCTL_DISK_SET_DRIVE_LAYOUT_EX
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
- IOCTL_DISK_SET_DRIVE_LAYOUT_EX
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_SET_DRIVE_LAYOUT_EX IOCTL


## -description


Partitions a disk according to the specified drive layout and partition information data.

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
  IOCTL_DISK_SET_DRIVE_LAYOUT_EX, // dwIoControlCode(LPVOID) lpInBuffer,            // input buffer
  (DWORD) nInBufferSize,          // size of the input buffer
  NULL,                           // lpOutBuffer0,                              // nOutBufferSize 
  (LPDWORD) lpBytesReturned,      // number of bytes returned
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/en-us/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



When specifying a <b>GUID</b> partition table (GPT) as the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-partition_style">PARTITION_STYLE</a> of the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-create_disk">CREATE_DISK</a> structure, an application should wait for the MSR partition arrival before sending the <b>IOCTL_DISK_SET_DRIVE_LAYOUT_EX</b> control code. For more information about device notification, see <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa">RegisterDeviceNotification</a>.

When creating and manipulating an Extended Boot Record (EBR), the first entry of the EBR should point to the logical drive that immediately follows the EBR and the next EBR should lie after the end of the current logical drive and before the start of the next logical drive.

If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout">IOCTL_DISK_SET_DRIVE_LAYOUT</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information_ex">DRIVE_LAYOUT_INFORMATION_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout_ex">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>
 

 

