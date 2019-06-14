---
UID: NI:winioctl.FSCTL_OPLOCK_BREAK_ACKNOWLEDGE
title: FSCTL_OPLOCK_BREAK_ACKNOWLEDGE
author: windows-sdk-content
description: Responds to notification that an exclusive opportunistic lock on a file is about to be broken. Use this operation to indicate that the file should receive a level 2 opportunistic lock.
old-location: fs\fsctl_oplock_break_acknowledge.htm
tech.root: FileIO
ms.assetid: 9f8fff44-99b4-4a8d-97f1-854b28fe2eb1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_OPLOCK_BREAK_ACKNOWLEDGE, FSCTL_OPLOCK_BREAK_ACKNOWLEDGE control, FSCTL_OPLOCK_BREAK_ACKNOWLEDGE control code [Files], _win32_fsctl_oplock_break_acknowledge, base.fsctl_oplock_break_acknowledge, fs.fsctl_oplock_break_acknowledge, winioctl/FSCTL_OPLOCK_BREAK_ACKNOWLEDGE
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
 - FSCTL_OPLOCK_BREAK_ACKNOWLEDGE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_OPLOCK_BREAK_ACKNOWLEDGE IOCTL


## -description


Responds to notification that an exclusive opportunistic lock on a file is about to be broken. Use 
    this operation to indicate that the file should receive a level 2 opportunistic lock.

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
DeviceIoControl( (HANDLE) hDevice,               // handle to file
                 FSCTL_OPLOCK_BREAK_ACKNOWLEDGE, // dwIoControlCode
                 NULL,                           // lpInBuffer
                 0,                              // nInBufferSize
                 NULL,                           // lpOutBuffer
                 0,                              // nOutBufferSize
                 (LPDWORD) lpBytesReturned,      // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
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
    server. Client applications requesting opportunistic locks from remote servers must not request them directly—the 
    network redirector transparently requests opportunistic locks for the application.

For the implications of overlapped I/O on this operation, see the Remarks section of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

<b>FSCTL_OPLOCK_BREAK_ACKNOWLEDGE</b> is a 
    response to notification that a level 1, batch, or filter opportunistic lock on an application's file has been 
    broken. It indicates to the server that the application should receive a level 2 opportunistic lock. If the 
    operation returns the error code <b>ERROR_IO_PENDING</b>, the server has granted the 
    application a level 2 lock on the file.

One alternative to using 
    <b>FSCTL_OPLOCK_BREAK_ACKNOWLEDGE</b> is to 
    indicate that the application is about to close the file anyway. Use the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending">FSCTL_OPBATCH_ACK_CLOSE_PENDING</a> control 
    code for this response.

Another alternative is to request to keep the file open but loose all locking, by means of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2">FSCTL_OPLOCK_BREAK_ACK_NO_2</a> control code.

Applications are notified that an opportunistic lock is broken by using the <b>hEvent</b> 
    member of the <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-_overlapped">OVERLAPPED</a> structure associated with the 
    file on which the opportunistic lock is broken. Applications may also use functions such as 
    <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> and 
    <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a>.

IIn Windows 8 and Windows Server 2012, this code is supported by the following technologies.

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



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending">FSCTL_OPBATCH_ACK_CLOSE_PENDING</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2">FSCTL_OPLOCK_BREAK_ACK_NO_2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-_overlapped">OVERLAPPED</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/ifs/oplock-semantics">Oplock Semantics</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/opportunistic-locks">Opportunistic Locks</a>
 

 

