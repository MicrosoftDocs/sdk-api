---
UID: NI:winioctl.FSCTL_REQUEST_OPLOCK
title: FSCTL_REQUEST_OPLOCK
description: Requests an opportunistic lock (oplock) on a file and acknowledges that an oplock break has occurred.
old-location: fs\fsctl_request_oplock.htm
tech.root: FileIO
ms.assetid: 9df94089-137a-4540-9f46-119408b362ba
ms.date: 12/05/2018
ms.keywords: FSCTL_REQUEST_OPLOCK, FSCTL_REQUEST_OPLOCK control, FSCTL_REQUEST_OPLOCK control code [Files], fs.fsctl_request_oplock, winioctl/FSCTL_REQUEST_OPLOCK
f1_keywords:
- winioctl/FSCTL_REQUEST_OPLOCK
dev_langs:
- c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- FSCTL_REQUEST_OPLOCK
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_REQUEST_OPLOCK IOCTL


## -description


Requests an opportunistic lock (oplock) on a file and acknowledges that an oplock break has 
    occurred.

To perform this operation, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function using the following 
    parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl( (HANDLE) hDevice,              // handle to file
                     FSCTL_REQUEST_OPLOCK,          // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
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



This operation is used only by client applications requesting an opportunistic lock (oplock) from a local 
    server. Client applications requesting opportunistic locks from remote servers must not request them 
    directly—the network redirector transparently requests opportunistic locks for the 
    application. An attempt to use this operation to request opportunistic locks from remote servers will result in 
    the request being denied.

The <b>FSCTL_REQUEST_OPLOCK</b> control code provides 
    more efficient functionality  than the following related control codes: 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1">FSCTL_REQUEST_OPLOCK_LEVEL_1</a>, 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2">FSCTL_REQUEST_OPLOCK_LEVEL_2</a>, 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_filter_oplock">FSCTL_REQUEST_FILTER_OPLOCK</a>, and 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_batch_oplock">FSCTL_REQUEST_BATCH_OPLOCK</a>. Requesting 
    different oplock levels can be performed repeatedly on the same handle without closing and reopening the handle 
    when using <b>FSCTL_REQUEST_OPLOCK</b>; the other control 
    codes require that the handle be closed and then reopened with 
    <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> to make such a change. This is accomplished by 
    manipulating the <b>RequestedOplockLevel</b> member of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-request_oplock_input_buffer">REQUEST_OPLOCK_INPUT_BUFFER</a> structure when 
    re-issuing the <b>FSCTL_REQUEST_OPLOCK</b> control 
    code.

The following table summarizes how the caching ability of oplock types available from 
     <b>FSCTL_REQUEST_OPLOCK</b> correspond to the level 2, 
     level 1, and batch oplocks.

<table>
<tr>
<th>Alternative control code</th>
<th>Equivalent <b>RequestedOplockLevel</b> flags value</th>
<th>Oplock type</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_batch_oplock">FSCTL_REQUEST_BATCH_OPLOCK</a>
</td>
<td><code>OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_WRITE | OPLOCK_LEVEL_CACHE_HANDLE</code></td>
<td>RWH</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1">FSCTL_REQUEST_OPLOCK_LEVEL_1</a>
</td>
<td><code>OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_WRITE </code></td>
<td>RW</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2">FSCTL_REQUEST_OPLOCK_LEVEL_2</a>
</td>
<td><code>OPLOCK_LEVEL_CACHE_READ</code></td>
<td>R</td>
</tr>
</table>
 

Using the <b>FSCTL_REQUEST_OPLOCK</b> control code with 
     the <b>RequestedOplockLevel</b> member set to 
     <code>OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_HANDLE</code> grants an oplock of 
     type <i>RH</i>. An RH oplock is similar to the filter oplock granted by the 
     <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_filter_oplock">FSCTL_REQUEST_FILTER_OPLOCK</a> control code. 
     However, note that the filter oplock allows only one client to hold an oplock on a file at a time; 
     <b>FSCTL_REQUEST_OPLOCK</b> allows multiple clients at a 
     time to have the <i>RH</i> lock on a file. Another difference is that 
     <b>FSCTL_REQUEST_FILTER_OPLOCK</b> requires an 
     oplock break acknowledgment before writes can occur, where 
     <b>FSCTL_REQUEST_OPLOCK</b> does not because the oplock 
     break notification is advisory-only and writes are allowed to go ahead without acknowledgment. For more 
     information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/ifs/breaking-oplocks">Breaking Oplocks</a>.

An <b>FSCTL_REQUEST_OPLOCK</b> control code fails if the 
    file is opened in non-overlapped (synchronous) mode.

For the implications of overlapped I/O on this operation, see the Remarks section of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

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
Yes

</td>
</tr>
</table>
 

Also, beginning in Windows 8 and Windows Server 2012, the <b>FSCTL_REQUEST_OPLOCK</b> control code can be used to request an oplock on a directory as well as a file. An oplock request on a directory may specify either <code>OPLOCK_LEVEL_CACHE_READ</code> or <code>OPLOCK_LEVEL_CACHE_READ | OPLOCK_LEVEL_CACHE_HANDLE</code> in the RequestedOplockLevel member.



An R or RH oplock on a directory breaks to None when the contents of an enumeration of the directory would change. For example, adding/deleting a file in the directory, changing the size of a file in the directory, modifying the timestamp of a file in the directory, etc., would all break the oplock on the directory. This oplock break does not require an acknowledgment before the changes in the directory may occur; it is advisory-only.



An RH oplock on a directory breaks to R when the directory itself is renamed or deleted. This oplock break does require an acknowledgment before the change to the directory can occur.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ifs/oplock-semantics">Oplock Semantics</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/opportunistic-locks">Opportunistic Locks</a>
 

 

