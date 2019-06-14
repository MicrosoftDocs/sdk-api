---
UID: NI:winioctl.FSCTL_MARK_HANDLE
title: FSCTL_MARK_HANDLE
author: windows-sdk-content
description: Marks a specified file or directory and its change journal record with information about changes to that file or directory.
old-location: fs\fsctl_mark_handle.htm
tech.root: FileIO
ms.assetid: c96b49d8-12f3-4281-9f9f-6621769359f0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_MARK_HANDLE, FSCTL_MARK_HANDLE control, FSCTL_MARK_HANDLE control code [Files], _win32_fsctl_mark_handle, base.fsctl_mark_handle, fs.fsctl_mark_handle, winioctl/FSCTL_MARK_HANDLE
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
 - FSCTL_MARK_HANDLE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_MARK_HANDLE IOCTL


## -description


Marks a specified file or directory and its change journal record with information about changes to 
    that file or directory.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    function using the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to file or directory
                 FSCTL_MARK_HANDLE,             // dwIoControlCode(LPVOID)lpInBuffer,            // input buffer
                 (DWORD)nInBufferSize,          // size of input buffer
                 NULL,                          // lpOutBuffer0,                             // nOutBufferSize(LPDWORD) lpBytesReturned,     // number of bytes returned
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



For the implications of overlapped I/O on this operation, see the Remarks section of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

<b>FSCTL_MARK_HANDLE</b> is the only change journal 
    operation that operates on an individual file or directory. It does not affect anything the user can do with the 
    item. Instead, it adds information to the file or directory, either providing information on how the operating 
    system changed the item or adding a private data stream to the item.

If there are any changes to the file or directory, then the information added with 
    <b>FSCTL_MARK_HANDLE</b> is also copied into the USN record 
    created for the file or directory. Note that these two operations can occur independently of each other—for 
    example, it is not necessary for a USN record to exist to be able to mark a file as unable to be defragmented (see 
    the reference page for <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-mark_handle_info">MARK_HANDLE_INFO</a> 
    for more information on this) and it is not necessary to mark a file or directory to update the contents of the 
    corresponding USN record. For details on the information with which 
    <b>FSCTL_MARK_HANDLE</b> can mark an item, see the reference 
    page for <b>MARK_HANDLE_INFO</b>.

It is not an error to use <b>FSCTL_MARK_HANDLE</b> while the 
    volume's change journal is being deleted or is inactive. The appropriate information is applied to the file or 
    directory regardless of the state of the change journal, as long as the change journal exists.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use 
    unbuffered I/O.

 The volume must be NTFS.

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
 

CsvFs always issues <b>USN_SOURCE_REPLICATION_MANAGEMENT</b> and <b>MARK_HANDLE_PROTECT_CLUSTERS</b> for the files eligible for direct IO.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/change-journals">Change Journals</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-mark_handle_info">MARK_HANDLE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-_overlapped">OVERLAPPED</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
 

 

