---
UID: NI:winioctl.FSCTL_WRITE_USN_CLOSE_RECORD
title: FSCTL_WRITE_USN_CLOSE_RECORD
description: Generates a record in the update sequence number (USN) change journal stream for the input file.
old-location: fs\fsctl_write_usn_close_record.htm
tech.root: FileIO
ms.assetid: d7e0ad05-8ad5-4672-bd32-5a3b1dd0a6ea
ms.date: 12/05/2018
ms.keywords: FSCTL_WRITE_USN_CLOSE_RECORD, FSCTL_WRITE_USN_CLOSE_RECORD control, FSCTL_WRITE_USN_CLOSE_RECORD control code [Files], _win32_fsctl_write_usn_close_record, base.fsctl_write_usn_close_record, fs.fsctl_write_usn_close_record, winioctl/FSCTL_WRITE_USN_CLOSE_RECORD
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
 - FSCTL_WRITE_USN_CLOSE_RECORD
 - winioctl/FSCTL_WRITE_USN_CLOSE_RECORD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_WRITE_USN_CLOSE_RECORD
---

# FSCTL_WRITE_USN_CLOSE_RECORD IOCTL


## -description

Generates a record in the update sequence number (USN) change journal stream for the input 
    file. This record will have the <b>USN_REASON_CLOSE</b> flag.

To perform this operation, call the 
    <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following 
    parameters.
<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI
DeviceIoControl( (HANDLE) hDevice,              // handle to volume
                 FSCTL_WRITE_USN_CLOSE_RECORD,  // dwIoControlCodeNULL,                          // lpInBuffer0,                             // nInBufferSize(LPVOID) lpOutBuffer,          // output buffer
                 (DWORD) nOutBufferSize,        // size of output buffer
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
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

For the implications of overlapped I/O on this operation, see the Remarks section for 
    <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.

You can use <b>FSCTL_WRITE_USN_CLOSE_RECORD</b> 
    to force a close record into the change journal for the input handle. The close record will contain any current 
    USN reasons for this file as well. The output buffer will return the USN value associated with this 
    operation.

For more information, see 
     <a href="/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal">Creating, Modifying, and Deleting a Change Journal</a>.

To retrieve a handle to a volume, call 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string in the following form:

&#92;&#92;.&#92;<i>X</i>:

In the preceding string, <i>X</i> is the letter identifying the drive on which the volume 
     appears. The volume must be NTFS 3.0 or later. To obtain the NTFS version of a volume, open a command prompt with 
     Administrator access rights and execute the following command:

<b>fsutil fsinfo ntfsinfo </b><i>X</i><b>:</b>

where <i>X</i> is the drive letter of the volume.

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
 

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If <b>FSCTL_WRITE_USN_CLOSE_RECORD</b> is called 
      with a handle that is locked by a transaction, it always fails.

## -see-also

<a href="/windows/desktop/FileIO/change-journals">Change Journals</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
