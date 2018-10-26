---
UID: NI:winioctl.IOCTL_DISK_REASSIGN_BLOCKS_EX
title: IOCTL_DISK_REASSIGN_BLOCKS_EX
author: windows-sdk-content
description: Directs the disk device to map one or more blocks to its spare-block pool.
old-location: fs\ioctl_disk_reassign_blocks_ex.htm
tech.root: fileio
ms.assetid: 126ffefa-165b-4ca1-a905-1aebc8e790c7
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IOCTL_DISK_REASSIGN_BLOCKS_EX, IOCTL_DISK_REASSIGN_BLOCKS_EX control, IOCTL_DISK_REASSIGN_BLOCKS_EX control code [Files], base.ioctl_disk_reassign_blocks_ex, fs.ioctl_disk_reassign_blocks_ex, winioctl/IOCTL_DISK_REASSIGN_BLOCKS_EX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
 - IOCTL_DISK_REASSIGN_BLOCKS_EX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_REASSIGN_BLOCKS_EX IOCTL


## -description


Directs the disk device to map one or more blocks to its spare-block pool.

To perform this operation, call the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following 
    parameters.

```cpp
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device 
                 IOCTL_DISK_REASSIGN_BLOCKS_EX, // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
                 (DWORD) nInBufferSize,         // size of input buffer 
                 (LPVOID) NULL,                 // lpOutBuffer(DWORD) 0,                     // nOutBufferSize(LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
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



The <a href="https://msdn.microsoft.com/48036bdc-3588-41a6-9dbb-4606bdfcb683">REASSIGN_BLOCKS_EX</a> structure that the 
    <b>IOCTL_DISK_REASSIGN_BLOCKS_EX</b> control code 
    uses supports 8-byte Logical Block Addresses (LBA). For compatibility, the 
    <a href="https://msdn.microsoft.com/57343bc9-9dd4-47a3-8130-07ea330eb4d3">IOCTL_DISK_REASSIGN_BLOCKS</a> control code and 
    <a href="https://msdn.microsoft.com/43d908fc-0e43-49ab-a96f-b6b0f491c99d">REASSIGN_BLOCKS</a> structure should be used where the 
    LBA fits in the 4-byte LBA that  the 
    <b>REASSIGN_BLOCKS</b> structure supports (typically drives 
    up to 2 TB).




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/57343bc9-9dd4-47a3-8130-07ea330eb4d3">IOCTL_DISK_REASSIGN_BLOCKS</a>



<a href="https://msdn.microsoft.com/43d908fc-0e43-49ab-a96f-b6b0f491c99d">REASSIGN_BLOCKS</a>



<a href="https://msdn.microsoft.com/48036bdc-3588-41a6-9dbb-4606bdfcb683">REASSIGN_BLOCKS_EX</a>
 

 

