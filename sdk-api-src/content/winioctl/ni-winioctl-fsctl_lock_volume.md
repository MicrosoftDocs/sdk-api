---
UID: NI:winioctl.FSCTL_LOCK_VOLUME
title: FSCTL_LOCK_VOLUME
author: windows-sdk-content
description: Locks a volume if it is not in use.
old-location: fs\fsctl_lock_volume.htm
tech.root: FileIO
ms.assetid: b59b5c5e-6719-47a8-8810-14b60204e5ed
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_LOCK_VOLUME, FSCTL_LOCK_VOLUME control, FSCTL_LOCK_VOLUME control code [Files], _win32_fsctl_lock_volume, base.fsctl_lock_volume, fs.fsctl_lock_volume, winioctl/FSCTL_LOCK_VOLUME
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
 - FSCTL_LOCK_VOLUME
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_LOCK_VOLUME IOCTL


## -description


Locks a volume if it is not in use. A locked volume can be accessed only through handles to the file object (*<i>hDevice</i>) that locks the volume. For more information, see the Remarks section.

To perform this operation, call the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to a volume
  (DWORD) FSCTL_LOCK_VOLUME,   // dwIoControlCodeNULL,                        // lpInBuffer0,                           // nInBufferSizeNULL,                        // lpOutBuffer0,                           // nOutBufferSize(LPDWORD) lpBytesReturned,   // number of bytes returned
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



The <i>hDevice</i> handle passed to <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> must be a handle to a volume, opened for direct access. To retrieve this handle, call 
<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> with the <i>lpFileName</i> parameter set to a string of the following form: 

\\.\<i>X</i>:

where <i>X</i> is a hard-drive partition letter, floppy disk drive, or CD-ROM drive. The application must also specify the <b>FILE_SHARE_READ</b> and <b>FILE_SHARE_WRITE</b> flags in the <i>dwShareMode</i> parameter of 
<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.

If the specified volume is a system volume or contains a page file, the operation fails.

If there are any open files on the volume, this operation will fail. Conversely, success of this operation indicates there are no open files.

This operation is useful for applications that need exclusive access to a volume for a period of time—for example, disk utility and backup programs.

A locked volume remains locked until one of the following occurs:

<ul>
<li>The application uses the 
<a href="https://msdn.microsoft.com/84ca7f8d-6a0a-43d6-9970-9c01099eaad4">FSCTL_UNLOCK_VOLUME</a> control code to unlock the volume.</li>
<li>The handle closes, either directly through 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>, or indirectly when a process terminates.</li>
</ul>
The system flushes all cached data to the volume before locking it. For example, any data held in a lazy-write cache is written to the volume.

The NTFS file system treats a locked volume as a dismounted volume. The <a href="https://msdn.microsoft.com/8828760c-9635-4c69-9867-c2f5314841e6">FSCTL_DISMOUNT_VOLUME</a> control code functions similarly but does not check for open files before dismounting. Note that without a successful lock operation, a dismounted volume may be remounted by any process at any time. This would not be an ideal state for performing a volume backup, for example.

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
 

On CsvFs Lock Volume, PNP notification will be sent only on the node where the lock request was issued. A lock will succeed only if the CsvFs filter on top of NTFS does not see any opened files.

After acquiring a lock on a CSV volume, you must close the handle used to lock that volume before opening a handle to the volume. Unlocking the volume by using <a href="https://msdn.microsoft.com/84ca7f8d-6a0a-43d6-9970-9c01099eaad4">FSCTL_UNLOCK_VOLUME</a> is not sufficient.




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/8828760c-9635-4c69-9867-c2f5314841e6">FSCTL_DISMOUNT_VOLUME</a>



<a href="https://msdn.microsoft.com/84ca7f8d-6a0a-43d6-9970-9c01099eaad4">FSCTL_UNLOCK_VOLUME</a>



<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
 

 

