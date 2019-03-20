---
UID: NI:winioctl.IOCTL_DISK_SET_PARTITION_INFO_EX
title: IOCTL_DISK_SET_PARTITION_INFO_EX (winioctl.h)
author: windows-sdk-content
description: Sets partition information for the specified disk partition, including layout information for AT and EFI (Extensible Firmware Interface) partitions.
old-location: fs\ioctl_disk_set_partition_info_ex.htm
tech.root: FileIO
ms.assetid: 6feec7a9-5b57-406b-bbea-04cf9cdaf56b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOCTL_DISK_SET_PARTITION_INFO_EX, IOCTL_DISK_SET_PARTITION_INFO_EX control, IOCTL_DISK_SET_PARTITION_INFO_EX control code [Files], _win32_ioctl_disk_set_partition_info_ex, base.ioctl_disk_set_partition_info_ex, fs.ioctl_disk_set_partition_info_ex, winioctl/IOCTL_DISK_SET_PARTITION_INFO_EX
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
 - IOCTL_DISK_SET_PARTITION_INFO_EX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_SET_PARTITION_INFO_EX IOCTL


## -description


Sets partition information for the specified disk partition, including layout information for AT and EFI (Extensible Firmware Interface) partitions.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  IOCTL_DISK_SET_PARTITION_INFO_EX, // dwIoControlCode(LPVOID) lpInBuffer,              // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
  NULL,                             // lpOutBuffer0,                                // nOutBufferSize(LPDWORD) lpBytesReturned,        // number of bytes returned
  (LPOVERLAPPED) lpOverlapped       // OVERLAPPED structure
);
```



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



<a href="https://msdn.microsoft.com/f84f8be6-2b01-4a20-8669-cb1a55c32907">IOCTL_DISK_GET_PARTITION_INFO_EX</a>



<a href="Http://go.microsoft.com/fwlink/p/?linkid=128030">SET_PARTITION_INFORMATION_EX</a>
 

 

