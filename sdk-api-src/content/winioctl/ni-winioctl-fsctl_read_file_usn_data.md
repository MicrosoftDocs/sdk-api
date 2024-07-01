---
UID: NI:winioctl.FSCTL_READ_FILE_USN_DATA
title: FSCTL_READ_FILE_USN_DATA
description: Retrieves the update sequence number (USN) change-journal information for the specified file or directory.
old-location: fs\fsctl_read_file_usn_data.htm
tech.root: FileIO
ms.assetid: 22c797c8-87c8-4d45-b163-4573e6ed17e1
ms.date: 12/05/2018
ms.keywords: FSCTL_READ_FILE_USN_DATA, FSCTL_READ_FILE_USN_DATA control, FSCTL_READ_FILE_USN_DATA control code [Files], base.fsctl_read_file_usn_data, fs.fsctl_read_file_usn_data, winioctl/FSCTL_READ_FILE_USN_DATA
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
 - FSCTL_READ_FILE_USN_DATA
 - winioctl/FSCTL_READ_FILE_USN_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_READ_FILE_USN_DATA
---

# FSCTL_READ_FILE_USN_DATA IOCTL


## -description

Retrieves the update sequence number (USN) change-journal information for the specified file or 
    directory.

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
DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                 (DWORD) FSCTL_READ_FILE_USN_DATA, // dwIoControlCode
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

If the call succeeds, the  members of the returned 
    <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a> or 
    <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v3">USN_RECORD_V3</a> structure are valid except for the following 
    members: <b>TimeStamp</b>, <b>Reason</b>, and 
    <b>SourceInfo</b>. The <b>Usn</b> member represents the last USN written 
    to the journal for this file or directory.

For more information, see 
     <a href="/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal">Creating, Modifying, and Deleting a Change Journal</a>.

To retrieve a handle to a volume, call 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string in the following form:

&#92;&#92;.&#92;<i>X</i>:

In the preceding string, <i>X</i> is the letter identifying the drive on which the volume 
     appears. The volume must be ReFS or NTFS 3.0 or later. To obtain the NTFS version of a volume, open a command prompt with 
     Administrator access rights and execute the following command:

<b>FSUtil.exe FSInfo NTFSInfo </b><i>X</i><b>:</b>

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

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD</a>



<a href="/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
