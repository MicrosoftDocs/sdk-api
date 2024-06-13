---
UID: NI:winioctl.FSCTL_QUERY_USN_JOURNAL
title: FSCTL_QUERY_USN_JOURNAL
description: Queries for information on the current update sequence number (USN) change journal, its records, and its capacity.
old-location: fs\fsctl_query_usn_journal.htm
tech.root: FileIO
ms.assetid: 9491b054-934a-4b76-bf77-f397b6386f82
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_USN_JOURNAL, FSCTL_QUERY_USN_JOURNAL control, FSCTL_QUERY_USN_JOURNAL control code [Files], _win32_fsctl_query_usn_journal, base.fsctl_query_usn_journal, fs.fsctl_query_usn_journal, winioctl/FSCTL_QUERY_USN_JOURNAL
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
 - FSCTL_QUERY_USN_JOURNAL
 - winioctl/FSCTL_QUERY_USN_JOURNAL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_QUERY_USN_JOURNAL
---

# FSCTL_QUERY_USN_JOURNAL IOCTL


## -description

Queries for information on the current update sequence number (USN) change journal, its records, and 
    its capacity.
<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       Device,          // handle to volume
                 (DWORD) FSCTL_QUERY_USN_JOURNAL,// dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer
                 (DWORD)        0,               // nInBufferSize
                 (LPVOID)       lpOutBuffer,     // output buffer
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
</td>
</tr>
</table></span></div>To perform this operation, call the 
    <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function using the following 
    parameters.

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

For more information, see 
     <a href="/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal">Creating, Modifying, and Deleting a Change Journal</a>.

To retrieve a handle to a volume, call 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string in the following form:

&#92;&#92;.&#92;<i>X</i>:

In the preceding string, <i>X</i> is the letter identifying the drive on which the volume 
    appears. The volume must be formatted with the NTFS filesystem.

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
Yes

</td>
</tr>
</table>
 

An application may experience false positives on CsvFs pause/resume.

## -see-also

<a href="/windows/desktop/FileIO/change-journals">Change Journals</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_journal_data_v0">USN_JOURNAL_DATA_V0</a>



<a href="/previous-versions/windows/desktop/legacy/hh802707(v=vs.85)">USN_JOURNAL_DATA_V1</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_journal_data_v2">USN_JOURNAL_DATA_V2</a>



<a href="/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
