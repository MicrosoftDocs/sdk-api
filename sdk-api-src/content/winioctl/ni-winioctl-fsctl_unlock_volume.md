---
UID: NI:winioctl.FSCTL_UNLOCK_VOLUME
title: FSCTL_UNLOCK_VOLUME
description: Unlocks a volume.
old-location: fs\fsctl_unlock_volume.htm
tech.root: FileIO
ms.assetid: 84ca7f8d-6a0a-43d6-9970-9c01099eaad4
ms.date: 12/05/2018
ms.keywords: FSCTL_UNLOCK_VOLUME, FSCTL_UNLOCK_VOLUME control, FSCTL_UNLOCK_VOLUME control code [Files], _win32_fsctl_unlock_volume, base.fsctl_unlock_volume, fs.fsctl_unlock_volume, winioctl/FSCTL_UNLOCK_VOLUME
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
 - FSCTL_UNLOCK_VOLUME
 - winioctl/FSCTL_UNLOCK_VOLUME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_UNLOCK_VOLUME
---

# FSCTL_UNLOCK_VOLUME IOCTL


## -description

Unlocks a volume.

To perform this operation, call the 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to a volume
  FSCTL_UNLOCK_VOLUME,         // dwIoControlCode
  NULL,                        // lpInBuffer
  0,                           // nInBufferSize
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
);
```

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

To lock a volume, use the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lock_volume">FSCTL_LOCK_VOLUME</a> control code.

The <i>hDevice</i> handle passed to <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> must be a handle to a volume, opened for direct access. To retrieve this handle, call 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the <i>lpFileName</i> parameter set to a string of the following form:

&#92;&#92;.&#92;<i>X</i>:

where <i>X</i> is a hard-drive partition letter, floppy disk drive, or CD-ROM drive. The application must also specify the <b>FILE_SHARE_READ</b> and <b>FILE_SHARE_WRITE</b> flags in the <i>dwShareMode</i> parameter of 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

IIn Windows 8 and Windows Server 2012, this code is supported by the following technologies.

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
 

PNP notification is issued only on the node where the FSCTL was issued.

After acquiring a lock on a CSV volume, you must close the handle used to lock that volume before opening a handle to the volume. Unlocking the volume by using <b>FSCTL_UNLOCK_VOLUME</b> is not sufficient.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_lock_volume">FSCTL_LOCK_VOLUME</a>



<a href="/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
