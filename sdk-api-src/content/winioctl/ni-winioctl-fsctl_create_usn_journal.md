---
UID: NI:winioctl.FSCTL_CREATE_USN_JOURNAL
title: FSCTL_CREATE_USN_JOURNAL
description: Creates an update sequence number (USN) change journal stream on a target volume, or modifies an existing change journal stream.
old-location: fs\fsctl_create_usn_journal.htm
tech.root: FileIO
ms.assetid: 92e737e6-dba6-47f1-a077-e303039e12eb
ms.date: 12/05/2018
ms.keywords: FSCTL_CREATE_USN_JOURNAL, FSCTL_CREATE_USN_JOURNAL control, FSCTL_CREATE_USN_JOURNAL control code [Files], _win32_fsctl_create_usn_journal, base.fsctl_create_usn_journal, fs.fsctl_create_usn_journal, winioctl/FSCTL_CREATE_USN_JOURNAL
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
 - FSCTL_CREATE_USN_JOURNAL
 - winioctl/FSCTL_CREATE_USN_JOURNAL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_CREATE_USN_JOURNAL
---

# FSCTL_CREATE_USN_JOURNAL IOCTL


## -description

Creates an update sequence number (USN) change journal stream on a target volume, or modifies an existing change journal 
    stream.
<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to volume
                 FSCTL_CREATE_USN_JOURNAL,      // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
                 (DWORD) nInBufferSize,         // size of input buffer
                 NULL,                          // lpOutBuffer
                 0,                             // nOutBufferSize(LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure</pre>
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

For the implications of overlapped I/O on this operation, see the Remarks section of the 
     <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

You can use <b>FSCTL_CREATE_USN_JOURNAL</b> to create 
     a new change journal stream for a volume. After the creation of the stream, the NTFS file system maintains a 
     change journal for that volume.

You can also use <b>FSCTL_CREATE_USN_JOURNAL</b> to 
     modify an existing change journal stream. If a change journal stream already exists, 
     <b>FSCTL_CREATE_USN_JOURNAL</b> sets it to the 
     characteristics provided in the 
     <a href="/windows/desktop/api/winioctl/ns-winioctl-create_usn_journal_data">CREATE_USN_JOURNAL_DATA</a> 
     structure. The change journal stream eventually gets larger or is trimmed to the new size limit that 
     <a href="/windows/desktop/api/winioctl/ns-winioctl-create_usn_journal_data">CREATE_USN_JOURNAL_DATA</a> 
     imposes.

For more information, see 
     <a href="/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal">Creating, Modifying, and Deleting a Change Journal</a>.

To retrieve a handle to a volume, call 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string in the following form:

&#92;&#92;.&#92;<i>X</i>:

In the preceding string, <i>X</i> is the letter identifying the drive on which the 
     volume appears. The volume must be NTFS 3.0 or later. To obtain the NTFS version of a volume, open a command 
     prompt with Administrator access rights and execute the following command:

<b>fsutil fsinfo ntfsinfo </b><i>X</i><b>:</b>

where <i>X</i> is the drive letter of the volume.

In Windows Server 2012, this function is supported by the following technologies.

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
Yes

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-create_usn_journal_data">CREATE_USN_JOURNAL_DATA</a>



<a href="/windows/desktop/FileIO/change-journals">Change Journals</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
