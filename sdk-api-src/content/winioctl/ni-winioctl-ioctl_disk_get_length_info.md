---
UID: NI:winioctl.IOCTL_DISK_GET_LENGTH_INFO
title: IOCTL_DISK_GET_LENGTH_INFO
author: windows-sdk-content
description: Retrieves the length of the specified disk, volume, or partition.
old-location: fs\ioctl_disk_get_length_info.htm
tech.root: fileio
ms.assetid: 8d4bd6e3-f0f3-40d6-b0ba-75155282f64a
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IOCTL_DISK_GET_LENGTH_INFO, IOCTL_DISK_GET_LENGTH_INFO control, IOCTL_DISK_GET_LENGTH_INFO control code [Files], _win32_ioctl_disk_get_length_info, base.ioctl_disk_get_length_info, fs.ioctl_disk_get_length_info, winioctl/IOCTL_DISK_GET_LENGTH_INFO
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GET_LENGTH_INFO IOCTL


## -description


Retrieves the length of the specified disk, volume, or partition.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
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



Volume handles do not have access to the full volume. To read or write to the last few sectors of a volume, you must call <a href="https://msdn.microsoft.com/7d895367-f48f-47db-9ef9-cf20d0ea6782">FSCTL_ALLOW_EXTENDED_DASD_IO</a>, which instructs the file system to not perform any boundary checks.


This operation should be used instead of 
<a href="https://msdn.microsoft.com/f84f8be6-2b01-4a20-8669-cb1a55c32907">IOCTL_DISK_GET_PARTITION_INFO_EX</a> for volumes that do not have partition info—such as partition type or number of hidden sectors.




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/a0d2a5bc-32e0-47d6-a4f0-84bd7f6bb746">GET_LENGTH_INFORMATION</a>
 

 

