---
UID: NI:winioctl.FSCTL_OPBATCH_ACK_CLOSE_PENDING
title: FSCTL_OPBATCH_ACK_CLOSE_PENDING
author: windows-sdk-content
description: Notifies a server that a client application is ready to close a file.
old-location: fs\fsctl_opbatch_ack_close_pending.htm
tech.root: FileIO
ms.assetid: 09014adb-e65e-4e9c-9f29-4bdbe61ea695
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_OPBATCH_ACK_CLOSE_PENDING, FSCTL_OPBATCH_ACK_CLOSE_PENDING control, FSCTL_OPBATCH_ACK_CLOSE_PENDING control code [Files], _win32_fsctl_opbatch_ack_close_pending, base.fsctl_opbatch_ack_close_pending, fs.fsctl_opbatch_ack_close_pending, winioctl/FSCTL_OPBATCH_ACK_CLOSE_PENDING
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
 - FSCTL_OPBATCH_ACK_CLOSE_PENDING
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_OPBATCH_ACK_CLOSE_PENDING IOCTL


## -description


Notifies a server that a client application is ready to close a file. Use this operation after notification that an opportunistic lock on a file is ready to be broken. 

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> function by using the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to file
  FSCTL_OPBATCH_ACK_CLOSE_PENDING, // dwIoControlCodeNULL,                            // lpInBuffer0,                               // nInBufferSizeNULL,                            // lpOutBuffer0,                               // nOutBufferSize(LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);</pre>
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



Before you call this function do not make assumptions about the number of available virtual channels, because the system and other plug-ins might have reserved virtual channels. Always check for a <b>CHANNEL_RC_TOO_MANY_CHANNELS</b> return code after calling this function.
			

For the implications of overlapped I/O on this operation, see the Remarks section of the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> topic.

Use the 
<b>FSCTL_OPBATCH_ACK_CLOSE_PENDING</b> control code when you are notified that an opportunistic lock on a file is ready to be broken, and you intend to close the file soon. This operation does not request a new opportunistic lock.

If you do not intend to close a file, you can use the 
<a href="https://msdn.microsoft.com/9f8fff44-99b4-4a8d-97f1-854b28fe2eb1">FSCTL_OPLOCK_BREAK_ACKNOWLEDGE</a> or 
<a href="https://msdn.microsoft.com/1624fa94-fcf4-4804-b659-84de5ccc77dc">FSCTL_OPLOCK_BREAK_ACK_NO_2</a> control code to respond to the notification. The former, used if the lock being broken is an exclusive opportunistic lock, indicates the file should receive a level 2 opportunistic lock instead. The latter requests the file be kept open but loses all locking.
			

Applications are notified that an opportunistic lock is broken by using the <b>hEvent</b> member of the 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that is associated with a file on which an opportunistic lock is broken. Applications can also use functions such as 
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> and 
<a href="https://msdn.microsoft.com/1e2a3bf0-a73e-4406-99ac-32652f7f5b25">HasOverlappedIoCompleted</a>.

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




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/9f8fff44-99b4-4a8d-97f1-854b28fe2eb1">FSCTL_OPLOCK_BREAK_ACKNOWLEDGE</a>



<a href="https://msdn.microsoft.com/1624fa94-fcf4-4804-b659-84de5ccc77dc">FSCTL_OPLOCK_BREAK_ACK_NO_2</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/1e2a3bf0-a73e-4406-99ac-32652f7f5b25">HasOverlappedIoCompleted</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/b4c2f5f0-a29b-4598-a49b-da99e93d2991">Opportunistic Locks</a>
 

 

