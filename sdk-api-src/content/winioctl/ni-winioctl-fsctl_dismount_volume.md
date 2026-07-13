---
UID: NI:winioctl.FSCTL_DISMOUNT_VOLUME
title: FSCTL_DISMOUNT_VOLUME
description: Dismounts a volume regardless of whether or not the volume is currently in use. For more information, see the Remarks section.
old-location: fs\fsctl_dismount_volume.htm
tech.root: FileIO
ms.assetid: 8828760c-9635-4c69-9867-c2f5314841e6
ms.date: 12/05/2018
ms.keywords: FSCTL_DISMOUNT_VOLUME, FSCTL_DISMOUNT_VOLUME control, FSCTL_DISMOUNT_VOLUME control code [Files], _win32_fsctl_dismount_volume, base.fsctl_dismount_volume, fs.fsctl_dismount_volume, winioctl/FSCTL_DISMOUNT_VOLUME
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - FSCTL_DISMOUNT_VOLUME
 - winioctl/FSCTL_DISMOUNT_VOLUME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_DISMOUNT_VOLUME
---

# FSCTL_DISMOUNT_VOLUME IOCTL


## -description

Dismounts a volume regardless of whether or not the volume is currently in use. For more information, see the Remarks section.

To perform this operation, call the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to a volume
  (DWORD) FSCTL_DISMOUNT_VOLUME,   // dwIoControlCodeNULL,                        // lpInBuffer0,                           // nInBufferSizeNULL,                        // lpOutBuffer0,                           // nOutBufferSize(LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);</pre>
</td>
</tr>
</table></span></div>

## -ioctlparameters

### -input-buffer


### -input-buffer-length


### -output-buffer


### -output-buffer-length


### -in-out-buffer


### -inout-buffer-length


### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

The <b>FSCTL_DISMOUNT_VOLUME</b> control code will attempt to dismount a volume regardless of whether or not any other processes are using the volume, which can have unpredictable results for those processes if they do not hold a lock on the volume. For information about locking a volume, see <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lock_volume">FSCTL_LOCK_VOLUME</a>.

The <i>hDevice</i> handle passed to 
     <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> must be a handle to a volume, opened 
     for direct access. To retrieve a volume handle, call 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string of the following form:

&#92;&#92;.&#92;<i>X</i>:

where <i>X</i> is a hard-drive partition letter, floppy disk drive, or CD-ROM drive. The 
     application must also specify the <b>FILE_SHARE_READ</b> and 
     <b>FILE_SHARE_WRITE</b> flags in the <i>dwShareMode</i> parameter of 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

If the specified volume is a system volume or contains a page file, the operation fails.

If the specified volume is locked by another process, the operation fails. To prevent another process from 
    locking the volume, lock it as soon as you open it.

A dismounted volume has the following properties:

<ul>
<li>There are no open files.</li>
<li>The operating system does detect the volume.</li>
</ul>
The operating system tries to mount an unmounted volume as soon as an attempt is made to access it. For 
    example, a call to <a href="/windows/desktop/api/fileapi/nf-fileapi-getlogicaldrives">GetLogicalDrives</a> triggers the 
    operating system to mount unmounted volumes.

Dismounting a volume is useful when a volume needs to disappear for a while. For example, an application that 
    changes a volume file system from the FAT file system to the NTFS file system might use the following 
    procedure.

<p class="proch"><b>To change a volume file system</b>

<ol>
<li>Open a volume.</li>
<li>Lock the volume.</li>
<li>Format the volume.</li>
<li>Dismount the volume.</li>
<li>Unlock the volume.</li>
<li>Close the volume handle.</li>
</ol>
A dismounting operation removes the volume from the FAT file system awareness. When the operating system 
    mounts the volume, it appears as an NTFS file system volume.

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
 

On CsvFs the node where dismount is issued will see a normal dismount sequence. On all other nodes FS will invalidate all the opened files.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread">ExitThread</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lock_volume">FSCTL_LOCK_VOLUME</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getlogicaldrives">GetLogicalDrives</a>



<a href="/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
