---
UID: NI:winioctl.FSCTL_ENUM_USN_DATA
title: FSCTL_ENUM_USN_DATA
author: windows-sdk-content
description: Enumerates the update sequence number (USN) data between two specified boundaries to obtain master file table (MFT) records.
old-location: fs\fsctl_enum_usn_data.htm
tech.root: FileIO
ms.assetid: 44d20401-a2ed-4756-9fda-878a24eab7c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_ENUM_USN_DATA, FSCTL_ENUM_USN_DATA control, FSCTL_ENUM_USN_DATA control code [Files], _win32_fsctl_enum_usn_data, base.fsctl_enum_usn_data, fs.fsctl_enum_usn_data, winioctl/FSCTL_ENUM_USN_DATA
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
 - FSCTL_ENUM_USN_DATA
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_ENUM_USN_DATA IOCTL


## -description


Enumerates  the update sequence number (USN) data between two specified boundaries to obtain master 
    file table (MFT) records.

To perform this operation, call the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function with the following 
    parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
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

To enumerate files on a volume, use the 
    <b>FSCTL_ENUM_USN_DATA</b> operation one or more times. On the 
     first call, set the starting point, the <b>StartFileReferenceNumber</b> member of the 
     <a href="https://msdn.microsoft.com/bd098d10-b30f-44b0-a379-2d57e33fe1c9">MFT_ENUM_DATA</a> structure, to 
     <code>(DWORDLONG)0</code>. Each call to 
     <b>FSCTL_ENUM_USN_DATA</b> retrieves the starting point for 
     the subsequent call as the first entry in the output buffer.

By comparing To identify recent changes to a volume, use the 
    <a href="https://msdn.microsoft.com/205de464-7e96-477b-9115-e819719b160e">FSCTL_READ_USN_JOURNAL</a> control code.

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
Yes

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/205de464-7e96-477b-9115-e819719b160e">FSCTL_READ_USN_JOURNAL</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/bd098d10-b30f-44b0-a379-2d57e33fe1c9">MFT_ENUM_DATA</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/1747453d-fd18-4853-a953-47131f3067ae">USN_RECORD</a>



<a href="https://msdn.microsoft.com/87f39e1c-3ebf-4c6f-a842-699ec3c45e76">Volume Management Control Codes</a>
 

 

