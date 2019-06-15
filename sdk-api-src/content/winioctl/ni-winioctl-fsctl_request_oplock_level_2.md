---
UID: NI:winioctl.FSCTL_REQUEST_OPLOCK_LEVEL_2
title: FSCTL_REQUEST_OPLOCK_LEVEL_2
author: windows-sdk-content
description: Requests a level 2 opportunistic lock on a file.
old-location: fs\fsctl_request_oplock_level_2.htm
tech.root: FileIO
ms.assetid: e7a36484-2ebc-4c91-b11f-e4ffb804dfa5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_REQUEST_OPLOCK_LEVEL_2, FSCTL_REQUEST_OPLOCK_LEVEL_2 control, FSCTL_REQUEST_OPLOCK_LEVEL_2 control code [Files], _win32_fsctl_request_oplock_level_2, base.fsctl_request_oplock_level_2, fs.fsctl_request_oplock_level_2, winioctl/FSCTL_REQUEST_OPLOCK_LEVEL_2
ms.topic: ioctl
f1_keywords: ["winioctl/FSCTL_REQUEST_OPLOCK_LEVEL_2"]
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
 - FSCTL_REQUEST_OPLOCK_LEVEL_2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_REQUEST_OPLOCK_LEVEL_2 IOCTL


## -description


Requests a level 2 opportunistic lock on a file.

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
                      FSCTL_REQUEST_OPLOCK_LEVEL_2,  // dwIoControlCodeNULL,                          // lpInBuffer0,                             // nInBufferSizeNULL,                          // lpOutBuffer0,                             // nOutBufferSize(LPDWORD) lpBytesReturned,     // number of bytes returned
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



This operation is used only by client applications requesting an opportunistic lock from a local server. 
    Client applications requesting opportunistic locks from remote servers must not request them directly—the network 
    redirector transparently requests opportunistic locks for the application. An attempt to use this operation to 
    request opportunistic locks from remote servers will result in the request being denied.

If a new oplock type is desired, the handle must be closed and a new handle reopened using 
    <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>, and 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> must be called on the new handle with 
    the desired <b>FSCTL_REQUEST_OPLOCK</b><i>_XXX</i> control code. To request 
    an oplock on a handle that can have the oplock type changed in place (the handle does not have to be closed and 
    reopened), use the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock">FSCTL_REQUEST_OPLOCK</a> control 
    code.

Use <b>FSCTL_REQUEST_OPLOCK_LEVEL_2</b> to 
    request a level 2 opportunistic lock on a file. A client file system can cache read data (but not write data) 
    locally as long as the level 2 lock is held.

The file system requires no acknowledgment from the application that requested the level 2 opportunistic lock 
    when the lock is broken. After the lock is broken, the network redirector is notified not to regard as valid any 
    cached data from the file. For more information, see 
    <a href="https://docs.microsoft.com/windows-hardware/drivers/ifs/breaking-oplocks">Breaking Oplocks</a>.

For more information, see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/types-of-opportunistic-locks">Types of Opportunistic Locks</a>.

For a comparison of the various oplock control codes, see 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock">FSCTL_REQUEST_OPLOCK</a>.

An <b>FSCTL_REQUEST_OPLOCK_LEVEL_2</b> control 
    code fails if the file is opened in nonoverlapped (synchronous) mode.

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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_request_oplock">FSCTL_REQUEST_OPLOCK</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-_overlapped">OVERLAPPED</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ifs/oplock-semantics">Oplock Semantics</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/opportunistic-locks">Opportunistic Locks</a>
 

 

