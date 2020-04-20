---
UID: NI:winioctl.IOCTL_DISK_GET_PARTITION_INFO_EX
title: IOCTL_DISK_GET_PARTITION_INFO_EX
description: Retrieves extended information about the type, size, and nature of a disk partition.helpviewer_keywords: ["IOCTL_DISK_GET_PARTITION_INFO_EX","IOCTL_DISK_GET_PARTITION_INFO_EX control","IOCTL_DISK_GET_PARTITION_INFO_EX control code [Files]","_win32_ioctl_disk_get_partition_info_ex","base.ioctl_disk_get_partition_info_ex","fs.ioctl_disk_get_partition_info_ex","winioctl/IOCTL_DISK_GET_PARTITION_INFO_EX"]
old-location: fs\ioctl_disk_get_partition_info_ex.htm
tech.root: FileIO
ms.assetid: f84f8be6-2b01-4a20-8669-cb1a55c32907
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_PARTITION_INFO_EX, IOCTL_DISK_GET_PARTITION_INFO_EX control, IOCTL_DISK_GET_PARTITION_INFO_EX control code [Files], _win32_ioctl_disk_get_partition_info_ex, base.ioctl_disk_get_partition_info_ex, fs.ioctl_disk_get_partition_info_ex, winioctl/IOCTL_DISK_GET_PARTITION_INFO_EX
f1_keywords:
- winioctl/IOCTL_DISK_GET_PARTITION_INFO_EX
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
- IOCTL_DISK_GET_PARTITION_INFO_EX
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GET_PARTITION_INFO_EX IOCTL


## -description


Retrieves extended information about the type, size, and nature of a disk 
    partition.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to a partition
  IOCTL_DISK_GET_PARTITION_INFO_EX, // dwIoControlCodeNULL,                             // lpInBuffer0,                                // nInBufferSize(LPVOID) lpOutBuffer,             // output buffer
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



The <b>IOCTL_DISK_GET_PARTITION_INFO_EX</b> 
    control code is supported on basic disks. It is only supported on dynamic disks that are boot or system disks, or have retained 
    entries in the partition table. The <a href="https://technet.microsoft.com/library/26a4a166-95fa-4faf-95bc-2d5345f4a57a">DiskPart.exe</a> command <b>RETAIN</b> can be used to do 
    this for other dynamic simple partitions.

The disk support can be summarized as follows.

<table>
<tr>
<th>Disk type</th>
<th>IOCTL_DISK_GET_PARTITION_INFO</th>
<th>IOCTL_DISK_GET_PARTITION_INFO_EX</th>
</tr>
<tr>
<td>Basic master boot record (MBR)</td>
<td>Yes</td>
<td>Yes</td>
</tr>
<tr>
<td>Basic GUID partition table (GPT)</td>
<td>No</td>
<td>Yes</td>
</tr>
<tr>
<td>Dynamic MBR boot/system</td>
<td>Yes</td>
<td>Yes</td>
</tr>
<tr>
<td>Dynamic MBR data</td>
<td>Yes</td>
<td>No</td>
</tr>
<tr>
<td>Dynamic GPT boot/system</td>
<td>No</td>
<td>Yes</td>
</tr>
<tr>
<td>Dynamic GPT data</td>
<td>No</td>
<td>No</td>
</tr>
</table>
 

Currently, GPT is supported only on 64-bit systems.

If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout">IOCTL_DISK_SET_DRIVE_LAYOUT</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-system-recognition">File System Recognition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_partition_info_ex">IOCTL_DISK_SET_PARTITION_INFO_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-partition_information_ex">PARTITION_INFORMATION_EX</a>
 

 

