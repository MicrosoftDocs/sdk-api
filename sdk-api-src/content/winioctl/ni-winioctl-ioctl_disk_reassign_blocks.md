---
UID: NI:winioctl.IOCTL_DISK_REASSIGN_BLOCKS
title: IOCTL_DISK_REASSIGN_BLOCKS
author: windows-sdk-content
description: Directs the disk device to map one or more blocks to its spare-block pool.
old-location: fs\ioctl_disk_reassign_blocks.htm
old-project: FileIO
ms.assetid: 57343bc9-9dd4-47a3-8130-07ea330eb4d3
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IOCTL_DISK_REASSIGN_BLOCKS, IOCTL_DISK_REASSIGN_BLOCKS control, IOCTL_DISK_REASSIGN_BLOCKS control code [Files], _win32_ioctl_disk_reassign_blocks, base.ioctl_disk_reassign_blocks, fs.ioctl_disk_reassign_blocks, winioctl/IOCTL_DISK_REASSIGN_BLOCKS
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STORAGE_QUERY_TYPE, *PSTORAGE_QUERY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	IOCTL_DISK_REASSIGN_BLOCKS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IOCTL_DISK_REASSIGN_BLOCKS IOCTL


## -description


Directs the disk device to map one or more blocks to its spare-block pool.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_DISK_REASSIGN_BLOCKS,  // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer 
  (DWORD) nInBufferSize,       // size of input buffer 
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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



The <a href="https://msdn.microsoft.com/library/windows/hardware/ff563962">REASSIGN_BLOCKS</a> structure that the 
    <b>IOCTL_DISK_REASSIGN_BLOCKS</b> control code uses only 
    supports drives where the Logical Block Address (LBA) fits into a 4-byte value (typically up to 2 TB). For larger 
    drives the <a href="https://msdn.microsoft.com/library/windows/hardware/jj602804">REASSIGN_BLOCKS_EX</a> structure that  the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/jj602797">IOCTL_DISK_REASSIGN_BLOCKS_EX</a> control code 
    uses supports 8-byte LBAs. For compatibility, the 
    <b>IOCTL_DISK_REASSIGN_BLOCKS</b> control code and 
    <b>REASSIGN_BLOCKS</b> structure should be used where 
    possible.




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj602797">IOCTL_DISK_REASSIGN_BLOCKS_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff563962">REASSIGN_BLOCKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj602804">REASSIGN_BLOCKS_EX</a>
 

 

