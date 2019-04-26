---
UID: NI:winioctl.FSCTL_SHRINK_VOLUME
title: FSCTL_SHRINK_VOLUME
author: windows-sdk-content
description: Signals that the volume is to be prepared to perform the shrink operation, the shrink operation is to be committed, or the shrink operation is to be terminated.
old-location: fs\fsctl_shrink_volume.htm
tech.root: FileIO
ms.assetid: cf545417-f933-4054-bed4-e6adbf822f9c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_SHRINK_VOLUME, FSCTL_SHRINK_VOLUME control, FSCTL_SHRINK_VOLUME control code [Files], fs.fsctl_shrink_volume, winioctl/FSCTL_SHRINK_VOLUME
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FSCTL_SHRINK_VOLUME
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SHRINK_VOLUME IOCTL


## -description


Signals that the volume is to be prepared to perform the shrink operation, the shrink operation is to be committed, or the shrink operation is to be terminated.

To perform this operation, call the 
   <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SHRINK_VOLUME, // dwIoControlCode(LPVOID) lpInBuffer,               // input buffer
  nInBufferSize,     // size of input buffer    
  NULL,                          // output buffer
  O,                             // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
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



This control code is only supported on NTFS and RAW file systems.


To complete a shrink operation, you must: 


<ol>
<li>Call <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> to open a handle to the volume.</li>
<li>Call <b>FSCTL_SHRINK_VOLUME</b>. Set the <b>ShrinkRequestType</b> member of the <a href="https://msdn.microsoft.com/91e2c4a1-7b95-49d9-9f28-c3ce4355f1ea">SHRINK_VOLUME_INFORMATION</a> structure to <b>ShrinkPrepare</b>. Set the <b>NewNumberOfSectors</b> member of the same structure to zero.  If this call succeeds, the filesystem will not allocate clusters beyond the end of the new volume length.</li>
<li>Call <a href="https://msdn.microsoft.com/ab7f81ac-a962-4e86-b426-b0082d251645">FSCTL_MOVE_FILE</a> on all files beyond the new number of sectors and move them within the valid range. You are responsible for moving any files that are affected by the shrink operation.  </li>
<li>Call <b>FSCTL_SHRINK_VOLUME</b>.  Set the <b>ShrinkRequestType</b> member of the <a href="https://msdn.microsoft.com/91e2c4a1-7b95-49d9-9f28-c3ce4355f1ea">SHRINK_VOLUME_INFORMATION</a> structure to <b>ShrinkCommit</b>. Set the <b>NewNumberOfSectors</b> member of the same structure to zero. If all files beyond the end of the new volume size have not been moved, the call fails with <b>STATUS_ALREADY_COMMITTED</b> (<b>ERROR_ACCESS_DENIED</b>).  Otherwise, the filesystem has now been shrunk.</li>
<li>Call  <a href="https://msdn.microsoft.com/bbcb0bee-a507-4abb-83df-328f3aa6caaa">IOCTL_DISK_GROW_PARTITION</a>. Set the <b>BytesToGrow</b> member of the <a href="https://msdn.microsoft.com/17ff8bbb-45a6-4ddd-a871-8519500c03a9">DISK_GROW_PARTITION</a> structure to the negative number that represents the number of bytes to remove.</li>
</ol>


In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
See comment

</td>
</tr>
</table>
 

Is supported only on the node that has NTFS mounted.




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/b941c5c8-39b4-4a5d-93e9-acbde7177d44">FSCTL_EXTEND_VOLUME</a>



<a href="https://msdn.microsoft.com/bbcb0bee-a507-4abb-83df-328f3aa6caaa">IOCTL_DISK_GROW_PARTITION</a>



<a href="https://msdn.microsoft.com/91e2c4a1-7b95-49d9-9f28-c3ce4355f1ea">SHRINK_VOLUME_INFORMATION</a>



<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
 

 

