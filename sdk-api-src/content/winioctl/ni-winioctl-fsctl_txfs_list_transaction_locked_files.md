---
UID: NI:winioctl.FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES
title: FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES
author: windows-sdk-content
description: Returns a list of all files currently locked by the specified transaction. If the return value is ERROR_MORE_DATA, it returns the length of the buffer required to hold the complete list of files at the time of this call.
old-location: fs\fsctl_txfs_list_transaction_locked_files.htm
tech.root: FileIO
ms.assetid: fdef45fd-b197-4428-96c5-ac91b43681b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES, FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES control, FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES control code [Files], fs.fsctl_txfs_list_transaction_locked_files, winioctl/FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES
ms.topic: ioctl
f1_keywords: ["winioctl/FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES"]
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
 - FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES IOCTL


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Returns a list of all files currently locked by the specified transaction. If the return value is 
    <b>ERROR_MORE_DATA</b>, it returns the length of the buffer required to hold the complete list 
    of files at the time of this call.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl( (HANDLE) hDevice,     // handle to device
  FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES, // dwIoControlCode(LPVOID) lpInBuffer,                      // input buffer
  (DWORD) nInBufferSize,                    // size of input buffer
  (LPVOID) lpOutBuffer,                     // output buffer
  (DWORD) nOutBufferSize,                   // size of output buffer
  (LPDWORD) lpBytesReturned,                // number of bytes returned
  (LPOVERLAPPED) lpOverlapped );            // OVERLAPPED structure</pre>
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



<b>FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES</b> 
    is a synchronous operation.

The file path names returned are relative to the volume root.

The number of files returned from one 
    call to the next can change depending on the number of active transactions at any given point in time. If this 
    call returns a request for a larger buffer, that size may or may not be adequate for the next call, based on the 
    number of active transactions at the time of the next call.

<b>ReFS:  </b>This code is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_txfs_list_transaction_locked_files">TXFS_LIST_TRANSACTION_LOCKED_FILES</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_txfs_list_transaction_locked_files_entry">TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY</a>
 

 

