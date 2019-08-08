---
UID: NI:winioctl.FSCTL_TXFS_TRANSACTION_ACTIVE
title: FSCTL_TXFS_TRANSACTION_ACTIVE
author: windows-sdk-content
description: Returns a Boolean value that indicates if there were any transactions active on the associated volume when the snapshot was taken. This call is only valid for read-only snapshot volumes.
old-location: fs\fsctl_txfs_transaction_active.htm
tech.root: FileIO
ms.assetid: c55802b7-9c56-48ee-9d0b-777f06fbeff1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_TRANSACTION_ACTIVE, FSCTL_TXFS_TRANSACTION_ACTIVE control, FSCTL_TXFS_TRANSACTION_ACTIVE control code [Files], fs.fsctl_txfs_transaction_active, winioctl/FSCTL_TXFS_TRANSACTION_ACTIVE
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_TXFS_TRANSACTION_ACTIVE
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- FSCTL_TXFS_TRANSACTION_ACTIVE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_TXFS_TRANSACTION_ACTIVE IOCTL


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Returns a Boolean value that  indicates if there were any transactions  active on the associated volume when the snapshot was taken.  This call is only valid for read-only snapshot volumes.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WINAPI 
BOOL 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 FSCTL_TXFS_TRANSACTION_ACTIVE, // dwIoControlCodeNULL,                          // lpInBuffer0,                             // nInBufferSize(LPVOID) lpOutBuffer,          // output buffer
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



<b>FSCTL_TXFS_TRANSACTION_ACTIVE</b> is a synchronous operation.

If the <b>TransactionsActiveAtSnapshot</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-txfs_transaction_active_info">TXFS_TRANSACTION_ACTIVE_INFO</a> structure is <b>TRUE</b>, you must remount the snapshot read/write, and run your recovery operations.

<b>ReFS:  </b>This code is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-txfs_transaction_active_info">TXFS_TRANSACTION_ACTIVE_INFO</a>
 

 

