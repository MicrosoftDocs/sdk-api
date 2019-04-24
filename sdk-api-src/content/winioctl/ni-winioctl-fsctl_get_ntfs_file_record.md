---
UID: NI:winioctl.FSCTL_GET_NTFS_FILE_RECORD
title: FSCTL_GET_NTFS_FILE_RECORD
author: windows-sdk-content
description: Retrieves the first file record that is in use and is of a lesser than or equal ordinal value to the requested file reference number.
old-location: fs\fsctl_get_ntfs_file_record.htm
tech.root: FileIO
ms.assetid: a7308fa4-0f69-4b69-bb89-5d645e2a9f6e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_NTFS_FILE_RECORD, FSCTL_GET_NTFS_FILE_RECORD control, FSCTL_GET_NTFS_FILE_RECORD control code [Files], _win32_fsctl_get_ntfs_file_record, base.fsctl_get_ntfs_file_record, fs.fsctl_get_ntfs_file_record, winioctl/FSCTL_GET_NTFS_FILE_RECORD
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
 - FSCTL_GET_NTFS_FILE_RECORD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_GET_NTFS_FILE_RECORD IOCTL


## -description


Retrieves the first file record that is in use and is of a lesser than or equal ordinal value to the 
    requested file reference number.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl( (HANDLE) hDevice,              // handle to device
                      FSCTL_GET_NTFS_FILE_RECORD,    // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
                      (DWORD) nInBufferSize,         // size of input buffer
                      (LPVOID) lpOutBuffer,          // output buffer
                      (DWORD) nOutBufferSize,        // size of output buffer
                      (LPDWORD) lpBytesReturned,     // number of bytes returned
                      (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure</pre>
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



This control code enumerates file identifiers in a downward fashion, and always returns a file record that is 
     in use. This means that the file identifier returned by this control code may not be the same as the file 
     identifier specified in the input buffer. For example, if file identifiers 1 through 9 and 15 are in use, file 
     identifiers 10 through 14 are not in use, and the file record corresponding to file identifier 15 is requested, 
     that file record is returned.

If the file records that correspond to file identifiers 10 through 14 are 
     requested, then the file record corresponding to file identifier 9 is returned. If any of the file records 
     corresponding to file identifiers 1 through 9 are requested, those file records is returned.

To determine the correct size of the output buffer pointed to by <i>lpOutBuffer</i>, first 
     call the <a href="https://msdn.microsoft.com/b5690b4f-3967-41d8-bf11-70f8b1da79ad">FSCTL_GET_NTFS_VOLUME_DATA</a> control code 
     to get the size of one file record. This is the value of the <b>BytesPerFileRecordSegment</b> 
     member of the returned 
     <a href="https://msdn.microsoft.com/9ca0fe72-162c-4d75-a2f3-e1c7c0b0152a">NTFS_VOLUME_DATA_BUFFER</a> structure. Then set 
     the size of the output buffer to the following expression:

<code>sizeof (NTFS_FILE_RECORD_OUTPUT_BUFFER) + sizeof (one file record) - 1</code>

If a file consists of multiple file records, they must be retrieved individually.

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
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
No

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/e27ded4b-d104-4244-b38e-5fed10d32e1e">File Management Control Codes</a>



<a href="https://msdn.microsoft.com/8b0317ca-6d0e-4a04-a05a-1627d22171e3">NTFS_FILE_RECORD_INPUT_BUFFER</a>



<a href="https://msdn.microsoft.com/e2597939-5159-4c35-9a1f-f3be43081d72">NTFS_FILE_RECORD_OUTPUT_BUFFER</a>
 

 

