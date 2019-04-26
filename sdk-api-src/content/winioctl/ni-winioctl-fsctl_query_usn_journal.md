---
UID: NI:winioctl.FSCTL_QUERY_USN_JOURNAL
title: FSCTL_QUERY_USN_JOURNAL
author: windows-sdk-content
description: Queries for information on the current update sequence number (USN) change journal, its records, and its capacity.
old-location: fs\fsctl_query_usn_journal.htm
tech.root: FileIO
ms.assetid: 9491b054-934a-4b76-bf77-f397b6386f82
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_USN_JOURNAL, FSCTL_QUERY_USN_JOURNAL control, FSCTL_QUERY_USN_JOURNAL control code [Files], _win32_fsctl_query_usn_journal, base.fsctl_query_usn_journal, fs.fsctl_query_usn_journal, winioctl/FSCTL_QUERY_USN_JOURNAL
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
 - FSCTL_QUERY_USN_JOURNAL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_QUERY_USN_JOURNAL IOCTL


## -description


Queries for information on the current update sequence number (USN) change journal, its records, and 
    its capacity.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       Device,          // handle to volume
                 (DWORD) FSCTL_QUERY_USN_JOURNAL,// dwIoControlCode(LPVOID)       NULL,            // lpInBuffer(DWORD)        0,               // nInBufferSize(LPVOID)       lpOutBuffer,     // output buffer
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
</td>
</tr>
</table></span></div>To perform this operation, call the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function using the following 
    parameters.


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



For the implications of overlapped I/O on this operation, see the Remarks section of the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> topic.

For more information, see 
     <a href="https://msdn.microsoft.com/26cbacc2-d26b-434b-91b5-31aedc96da13">Creating, Modifying, and Deleting a Change Journal</a>.

To retrieve a handle to a volume, call 
     <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string in the following form:

\\.\<i>X</i>:

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




<a href="https://msdn.microsoft.com/9a158c2b-da8e-4ca9-b3c1-2185cf41eb7d">Change Journals</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/6b75eab2-aa10-4b48-8918-e4b03b5d8564">USN_JOURNAL_DATA_V0</a>



<a href="https://msdn.microsoft.com/3ee0a76e-848c-4f41-9e8b-1ff023c7f3b3">USN_JOURNAL_DATA_V1</a>



<a href="https://msdn.microsoft.com/BBFA6D14-1423-45B0-83A0-62019D08507F">USN_JOURNAL_DATA_V2</a>



<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
 

 

