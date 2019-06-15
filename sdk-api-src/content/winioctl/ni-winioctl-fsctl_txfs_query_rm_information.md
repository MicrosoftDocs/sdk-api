---
UID: NI:winioctl.FSCTL_TXFS_QUERY_RM_INFORMATION
title: FSCTL_TXFS_QUERY_RM_INFORMATION
author: windows-sdk-content
description: Retrieves information for a resource manager (RM).
old-location: fs\fsctl_txfs_query_rm_information.htm
tech.root: FileIO
ms.assetid: 24e80fdb-9243-455a-a2bf-7bf9b0a61efb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_QUERY_RM_INFORMATION, FSCTL_TXFS_QUERY_RM_INFORMATION control, FSCTL_TXFS_QUERY_RM_INFORMATION control code [Files], base.fsctl_txfs_query_rm_information, fs.fsctl_txfs_query_rm_information, winioctl/FSCTL_TXFS_QUERY_RM_INFORMATION
ms.topic: ioctl
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
 - FSCTL_TXFS_QUERY_RM_INFORMATION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_TXFS_QUERY_RM_INFORMATION IOCTL


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Retrieves information for a resource manager (RM).

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  FSCTL_TXFS_QUERY_RM_INFORMATION, // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // bytes returned
  (LPOVERLAPPED) lpOverlapped );   // OVERLAPPED structure</pre>
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



<b>FSCTL_TXFS_QUERY_RM_INFORMATION</b> is a 
    synchronous operation.

If this call fails with <b>ERROR_BUFFER_TOO_SMALL</b>, the 
    <b>BytesRequired</b> member of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_txfs_query_rm_information">TXFS_QUERY_RM_INFORMATION</a> structure specifies 
    how large the buffer must be for the call to return successfully.

If you are writing an application that 
    supports remote Server Message Block Protocol clients, you must use this control code to use the resource 
    manager.

The  resource manager may be queried regardless of its state; if the RM is not started, 
    <b>ERROR_RM_NOT_ACTIVE</b> is returned. You can use the information about the active range of 
    the log to guide decisions about how much of the log to archive.

<b>ReFS:  </b>This code is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/transactional-ntfs-reference">Secondary Resource Managers for TxF Volumes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_txfs_query_rm_information">TXFS_QUERY_RM_INFORMATION</a>
 

 

