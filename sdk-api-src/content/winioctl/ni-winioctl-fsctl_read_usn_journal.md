---
UID: NI:winioctl.FSCTL_READ_USN_JOURNAL
title: FSCTL_READ_USN_JOURNAL
author: windows-sdk-content
description: Retrieves the set of update sequence number (USN) change journal records between two specified USN values.
old-location: fs\fsctl_read_usn_journal.htm
tech.root: FileIO
ms.assetid: 205de464-7e96-477b-9115-e819719b160e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_READ_USN_JOURNAL, FSCTL_READ_USN_JOURNAL control, FSCTL_READ_USN_JOURNAL control code [Files], _win32_fsctl_read_usn_journal, base.fsctl_read_usn_journal, fs.fsctl_read_usn_journal, winioctl/FSCTL_READ_USN_JOURNAL
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
 - FSCTL_READ_USN_JOURNAL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_READ_USN_JOURNAL IOCTL


## -description


Retrieves  the set of update sequence number (USN) change journal records between two specified USN 
    values.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to volume
                 (DWORD) FSCTL_READ_USN_JOURNAL, // dwIoControlCode(LPVOID)       lpInBuffer,      // input buffer
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

There are two <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> control codes that 
    return USN records, <b>FSCTL_READ_USN_JOURNAL</b> and 
    <a href="https://msdn.microsoft.com/44d20401-a2ed-4756-9fda-878a24eab7c3">FSCTL_ENUM_USN_DATA</a>. Use the latter when you want a 
    listing (enumeration) of the USN records between two USNs. Use the former when you want to select by USN.

For more information, see 
     <a href="https://msdn.microsoft.com/26cbacc2-d26b-434b-91b5-31aedc96da13">Creating, Modifying, and Deleting a Change Journal</a>.

To retrieve a handle to a volume, call 
     <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string in the following form:

\\.\<i>X</i>:

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
     <a href="https://msdn.microsoft.com/8946adb5-da47-4711-8800-86f323081c4c">Walking a Buffer of Change Journal Records</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9a158c2b-da8e-4ca9-b3c1-2185cf41eb7d">Change Journals</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/44d20401-a2ed-4756-9fda-878a24eab7c3">FSCTL_ENUM_USN_DATA</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/f88e71ba-6099-4928-9d71-732a4ca809bc">READ_USN_JOURNAL_DATA</a>



<a href="https://msdn.microsoft.com/1747453d-fd18-4853-a953-47131f3067ae">USN_RECORD</a>



<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
 

 

