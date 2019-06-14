---
UID: NI:winioctl.FSCTL_OPLOCK_BREAK_NOTIFY
title: FSCTL_OPLOCK_BREAK_NOTIFY
author: windows-sdk-content
description: Enables the calling application to wait for completion of an opportunistic lock break.
old-location: fs\fsctl_oplock_break_notify.htm
tech.root: FileIO
ms.assetid: 5d064b92-4d30-4213-a9f0-713fd0e7c321
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_OPLOCK_BREAK_NOTIFY, FSCTL_OPLOCK_BREAK_NOTIFY control, FSCTL_OPLOCK_BREAK_NOTIFY control code [Files], _win32_fsctl_oplock_break_notify, base.fsctl_oplock_break_notify, fs.fsctl_oplock_break_notify, winioctl/FSCTL_OPLOCK_BREAK_NOTIFY
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
 - FSCTL_OPLOCK_BREAK_NOTIFY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_OPLOCK_BREAK_NOTIFY IOCTL


## -description


Enables the calling application to wait for completion of an opportunistic lock break.

This operation is not useful to application developers and is documented here only for completeness. 
    <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> handles the problem that this operation was 
    designed to handle.

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
DeviceIoControl( (HANDLE) hDevice,              // handle to file
                 FSCTL_OPLOCK_BREAK_NOTIFY,     // dwIoControlCode
                 NULL,                          // lpInBuffer
                 0,                             // nInBufferSize
                 NULL,                          // lpOutBuffer
                 0,                             // nOutBufferSize
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



This operation is used only by client applications that have requested an opportunistic lock from a local 
    server. Client applications requesting opportunistic locks from remote servers must not request them 
    directly—the network redirector transparently requests opportunistic locks for the application.

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



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-_overlapped">OVERLAPPED</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ifs/oplock-semantics">Oplock Semantics</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/opportunistic-locks">Opportunistic Locks</a>
 

 

