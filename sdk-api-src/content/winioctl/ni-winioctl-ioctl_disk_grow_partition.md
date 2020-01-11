---
UID: NI:winioctl.IOCTL_DISK_GROW_PARTITION
title: IOCTL_DISK_GROW_PARTITION
description: Enlarges the specified partition.
old-location: fs\ioctl_disk_grow_partition.htm
tech.root: FileIO
ms.assetid: bbcb0bee-a507-4abb-83df-328f3aa6caaa
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_GROW_PARTITION, IOCTL_DISK_GROW_PARTITION control, IOCTL_DISK_GROW_PARTITION control code [Files], base.ioctl_disk_grow_partition, fs.ioctl_disk_grow_partition, winioctl/IOCTL_DISK_GROW_PARTITION
f1_keywords:
- winioctl/IOCTL_DISK_GROW_PARTITION
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
- IOCTL_DISK_GROW_PARTITION
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_DISK_GROW_PARTITION IOCTL


## -description


Enlarges the specified partition.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_DISK_GROW_PARTITION,   // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer0,                           // nOutBufferSize 
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



You can extend or shrink a live partition, and the partition can be open for sharing during the extend or shrink operation. 

You do not need to lock a partition that you are extending, nor do you need to shut down other applications or services during the extend operation.

For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-disk_grow_partition">DISK_GROW_PARTITION</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-disk_grow_partition">DISK_GROW_PARTITION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>
 

 

