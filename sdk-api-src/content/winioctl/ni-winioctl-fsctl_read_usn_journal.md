---
UID: NI:winioctl.FSCTL_READ_USN_JOURNAL
title: FSCTL_READ_USN_JOURNAL
description: Retrieves the set of update sequence number (USN) change journal records between two specified USN values.
old-location: fs\fsctl_read_usn_journal.htm
tech.root: FileIO
ms.assetid: 205de464-7e96-477b-9115-e819719b160e
ms.date: 12/05/2018
ms.keywords: FSCTL_READ_USN_JOURNAL, FSCTL_READ_USN_JOURNAL control, FSCTL_READ_USN_JOURNAL control code [Files], _win32_fsctl_read_usn_journal, base.fsctl_read_usn_journal, fs.fsctl_read_usn_journal, winioctl/FSCTL_READ_USN_JOURNAL
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
 - FSCTL_READ_USN_JOURNAL
 - winioctl/FSCTL_READ_USN_JOURNAL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_READ_USN_JOURNAL
---

# FSCTL_READ_USN_JOURNAL IOCTL


## -description

Retrieves  the set of update sequence number (USN) change journal records between two specified USN 
    values.
<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to volume
                 (DWORD) FSCTL_READ_USN_JOURNAL, // dwIoControlCode
                 (LPVOID)       lpInBuffer,      // input buffer
                 (DWORD)        nInBufferSize,   // size of input buffer
                 (LPVOID)       lpOutBuffer,     // output buffer
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
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

There are two <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> control codes that 
    return USN records, <b>FSCTL_READ_USN_JOURNAL</b> and 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_enum_usn_data">FSCTL_ENUM_USN_DATA</a>. Use the latter when you want a 
    listing (enumeration) of the USN records between two USNs. Use the former when you want to select by USN.

For more information, see 
     <a href="/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal">Creating, Modifying, and Deleting a Change Journal</a>.

To retrieve a handle to a volume, call 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string in the following form:

&#92;&#92;.&#92;<i>X</i>:

In the preceding string, <i>X</i> is the letter identifying the drive on which the volume 
     appears. The volume must be NTFS.

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
 

An application may experience false positives on CsvFs pause/resume.


#### Examples

For an example, see 
     <a href="/windows/desktop/FileIO/walking-a-buffer-of-change-journal-records">Walking a Buffer of Change Journal Records</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/FileIO/change-journals">Change Journals</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_enum_usn_data">FSCTL_ENUM_USN_DATA</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-read_usn_journal_data_v0">READ_USN_JOURNAL_DATA</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD</a>



<a href="/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
