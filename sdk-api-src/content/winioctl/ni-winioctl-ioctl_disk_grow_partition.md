---
UID: NI:winioctl.IOCTL_DISK_GROW_PARTITION
title: IOCTL_DISK_GROW_PARTITION
author: windows-sdk-content
description: Enlarges the specified partition.
old-location: fs\ioctl_disk_grow_partition.htm
tech.root: fileio
ms.assetid: bbcb0bee-a507-4abb-83df-328f3aa6caaa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOCTL_DISK_GROW_PARTITION, IOCTL_DISK_GROW_PARTITION control, IOCTL_DISK_GROW_PARTITION control code [Files], base.ioctl_disk_grow_partition, fs.ioctl_disk_grow_partition, winioctl/IOCTL_DISK_GROW_PARTITION
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
 - IOCTL_DISK_GROW_PARTITION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GROW_PARTITION IOCTL


## -description


Enlarges the specified partition.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_DISK_GROW_PARTITION,   // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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



You can extend or shrink a live partition, and the partition can be open for sharing during the extend or shrink operation. 

You do not need to lock a partition that you are extending, nor do you need to shut down other applications or services during the extend operation.

For more information, see <a href="https://msdn.microsoft.com/17ff8bbb-45a6-4ddd-a871-8519500c03a9">DISK_GROW_PARTITION</a>.




## -see-also




<a href="https://msdn.microsoft.com/17ff8bbb-45a6-4ddd-a871-8519500c03a9">DISK_GROW_PARTITION</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>
 

 

