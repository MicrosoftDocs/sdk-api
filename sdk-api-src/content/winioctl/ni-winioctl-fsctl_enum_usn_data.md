---
UID: NI:winioctl.FSCTL_ENUM_USN_DATA
title: FSCTL_ENUM_USN_DATA
description: Enumerates the update sequence number (USN) data between two specified boundaries to obtain master file table (MFT) records.
old-location: fs\fsctl_enum_usn_data.htm
tech.root: FileIO
ms.assetid: 44d20401-a2ed-4756-9fda-878a24eab7c3
ms.date: 12/05/2018
ms.keywords: FSCTL_ENUM_USN_DATA, FSCTL_ENUM_USN_DATA control, FSCTL_ENUM_USN_DATA control code [Files], _win32_fsctl_enum_usn_data, base.fsctl_enum_usn_data, fs.fsctl_enum_usn_data, winioctl/FSCTL_ENUM_USN_DATA
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
 - FSCTL_ENUM_USN_DATA
 - winioctl/FSCTL_ENUM_USN_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_ENUM_USN_DATA
---

# FSCTL_ENUM_USN_DATA IOCTL


## -description

Enumerates  the update sequence number (USN) data between two specified boundaries to obtain master 
    file table (MFT) records.

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
                 (DWORD) FSCTL_ENUM_USN_DATA,   // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
                 (DWORD) nInBufferSize,         // size of input buffer
                 (LPVOID) lpOutBuffer,          // output buffer
                 (DWORD) nOutBufferSize,        // size of output buffer
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure);</pre>
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

To enumerate files on a volume, use the 
    <b>FSCTL_ENUM_USN_DATA</b> operation one or more times. On the 
     first call, set the starting point, the <b>StartFileReferenceNumber</b> member of the 
     <a href="/windows/desktop/api/winioctl/ns-winioctl-mft_enum_data_v0">MFT_ENUM_DATA</a> structure, to 
     <code>(DWORDLONG)0</code>. Each call to 
     <b>FSCTL_ENUM_USN_DATA</b> retrieves the starting point for 
     the subsequent call as the first entry in the output buffer.

By comparing To identify recent changes to a volume, use the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a> control code.

To retrieve a handle to a volume, call 
     <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> with the 
     <i>lpFileName</i> parameter set to a string in the following form:

\\\\.&#92;<i>X</i>:

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
Yes

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_read_usn_journal">FSCTL_READ_USN_JOURNAL</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-mft_enum_data_v0">MFT_ENUM_DATA</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD</a>



<a href="/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
