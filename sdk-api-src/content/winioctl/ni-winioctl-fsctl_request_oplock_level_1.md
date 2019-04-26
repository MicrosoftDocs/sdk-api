---
UID: NI:winioctl.FSCTL_REQUEST_OPLOCK_LEVEL_1
title: FSCTL_REQUEST_OPLOCK_LEVEL_1
author: windows-sdk-content
description: Requests a level 1 opportunistic lock on a file.
old-location: fs\fsctl_request_oplock_level_1.htm
tech.root: FileIO
ms.assetid: 625830b1-d99a-49cb-b072-303f076d4d3e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_REQUEST_OPLOCK_LEVEL_1, FSCTL_REQUEST_OPLOCK_LEVEL_1 control, FSCTL_REQUEST_OPLOCK_LEVEL_1 control code [Files], _win32_fsctl_request_oplock_level_1, base.fsctl_request_oplock_level_1, fs.fsctl_request_oplock_level_1, winioctl/FSCTL_REQUEST_OPLOCK_LEVEL_1
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
 - FSCTL_REQUEST_OPLOCK_LEVEL_1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_REQUEST_OPLOCK_LEVEL_1 IOCTL


## -description


Requests a level 1 opportunistic lock on a file.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function using the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl( (HANDLE) hDevice,              // handle to file
                      FSCTL_REQUEST_OPLOCK_LEVEL_1,  // dwIoControlCodeNULL,                          // lpInBuffer0,                             // nInBufferSizeNULL,                          // lpOutBuffer0,                             // nOutBufferSize(LPDWORD) lpBytesReturned,     // number of bytes returned
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
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>, and 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> must be called on the new handle with 
    the desired <b>FSCTL_REQUEST_OPLOCK</b><i>_XXX</i> control code. To request 
    an oplock on a handle that can have the oplock type changed in place (the handle does not have to be closed and 
    reopened), use the <a href="https://msdn.microsoft.com/9df94089-137a-4540-9f46-119408b362ba">FSCTL_REQUEST_OPLOCK</a> control 
    code.

Use <b>FSCTL_REQUEST_OPLOCK_LEVEL_1</b> to 
    request a level 1 opportunistic lock on a file. A client file system can cache both read data or write data 
    locally as long as the level 1 lock is held.

The level 1 oplock owner must acknowledge an 
    <a href="ifsk.breaking_oplocks">oplock break</a> before any operation that is incompatible 
    with a level 1 oplock can go through on another handle. After the lock is broken, the network redirector is 
    notified not to regard as valid any cached data from the file.

For more information, see 
    <a href="https://msdn.microsoft.com/06136348-0c08-4e9c-9c96-fd3af33cbdc0">Types of Opportunistic Locks</a>.

For a comparison of the various oplock control codes, see 
    <a href="https://msdn.microsoft.com/9df94089-137a-4540-9f46-119408b362ba">FSCTL_REQUEST_OPLOCK</a>.

An <b>FSCTL_REQUEST_OPLOCK_LEVEL_1</b> control 
    code fails if the file is opened in non-overlapped (synchronous) mode.

For the implications of overlapped I/O on this operation, see the Remarks section of the 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> topic.

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




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/9df94089-137a-4540-9f46-119408b362ba">FSCTL_REQUEST_OPLOCK</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="ifsk.oplock_semantics">Oplock Semantics</a>



<a href="https://msdn.microsoft.com/b4c2f5f0-a29b-4598-a49b-da99e93d2991">Opportunistic Locks</a>
 

 

