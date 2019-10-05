---
UID: NI:winioctl.IOCTL_DISK_GET_LENGTH_INFO
title: IOCTL_DISK_GET_LENGTH_INFO
author: windows-sdk-content
description: Retrieves the length of the specified disk, volume, or partition.
old-location: fs\ioctl_disk_get_length_info.htm
tech.root: FileIO
ms.assetid: 8d4bd6e3-f0f3-40d6-b0ba-75155282f64a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GET_LENGTH_INFO, IOCTL_DISK_GET_LENGTH_INFO control, IOCTL_DISK_GET_LENGTH_INFO control code [Files], _win32_ioctl_disk_get_length_info, base.ioctl_disk_get_length_info, fs.ioctl_disk_get_length_info, winioctl/IOCTL_DISK_GET_LENGTH_INFO
ms.topic: ioctl
f1_keywords:
- winioctl/IOCTL_DISK_GET_LENGTH_INFO
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
- IOCTL_DISK_GET_LENGTH_INFO
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GET_LENGTH_INFO IOCTL


## -description


Retrieves the length of the specified disk, volume, or partition.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to device
  IOCTL_DISK_GET_LENGTH_INFO,    // dwIoControlCodeNULL,                          // lpInBuffer0,                             // nInBufferSize(LPVOID) lpOutBuffer,          // output buffer
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




## -remarks



Volume handles do not have access to the full volume. To read or write to the last few sectors of a volume, you must call <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_allow_extended_dasd_io">FSCTL_ALLOW_EXTENDED_DASD_IO</a>, which instructs the file system to not perform any boundary checks.


This operation should be used instead of 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info_ex">IOCTL_DISK_GET_PARTITION_INFO_EX</a> for volumes that do not have partition info—such as partition type or number of hidden sectors.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-get_length_information">GET_LENGTH_INFORMATION</a>
 

 

