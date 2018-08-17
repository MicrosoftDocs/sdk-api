---
UID: NI:winioctl.IOCTL_DISK_SET_PARTITION_INFO
title: IOCTL_DISK_SET_PARTITION_INFO
author: windows-sdk-content
description: Sets partition information for the specified disk partition.
old-location: fs\ioctl_disk_set_partition_info.htm
old-project: fileio
ms.assetid: 868cad92-fa88-4a5a-98bb-92e73c115a22
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOCTL_DISK_SET_PARTITION_INFO, IOCTL_DISK_SET_PARTITION_INFO control, IOCTL_DISK_SET_PARTITION_INFO control code [Files], _win32_ioctl_disk_set_partition_info, base.ioctl_disk_set_partition_info, fs.ioctl_disk_set_partition_info, winioctl/IOCTL_DISK_SET_PARTITION_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: WRITE_THROUGH
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_DISK_SET_PARTITION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_DISK_SET_PARTITION_INFO IOCTL


## -description


Sets partition information for the specified disk partition.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.

<b>IOCTL_DISK_SET_PARTITION_INFO</b> has been superseded by 
<a href="https://msdn.microsoft.com/6feec7a9-5b57-406b-bbea-04cf9cdaf56b">IOCTL_DISK_SET_PARTITION_INFO_EX</a>, which retrieves layout information for AT and EFI (Extensible Firmware Interface) partitions.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_DISK_SET_PARTITION_INFO,   // dwIoControlCode(LPVOID) lpInBuffer,             // input buffer 
  (DWORD) nInBufferSize,           // size of input buffer 
  NULL,                            // lpOutBuffer0,                               // nOutBufferSize(LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
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



If the partition is on a disk formatted as type master boot record (MBR), partition size totals are limited. For more information, see the Remarks section of <a href="https://msdn.microsoft.com/8cace6a5-666a-4d35-a557-6bf0564dbe58">IOCTL_DISK_SET_DRIVE_LAYOUT</a>.




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/24053a1a-8cf8-4aa8-a611-15c9fae0a36d">IOCTL_DISK_GET_PARTITION_INFO</a>



<a href="https://msdn.microsoft.com/6feec7a9-5b57-406b-bbea-04cf9cdaf56b">IOCTL_DISK_SET_PARTITION_INFO_EX</a>



<a href="https://msdn.microsoft.com/cc04868c-cb9c-455f-a0df-bde6a133eb60">SET_PARTITION_INFORMATION</a>
 

 

