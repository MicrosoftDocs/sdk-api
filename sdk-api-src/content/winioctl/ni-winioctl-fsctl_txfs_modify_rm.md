---
UID: NI:winioctl.FSCTL_TXFS_MODIFY_RM
title: FSCTL_TXFS_MODIFY_RM
author: windows-sdk-content
description: Sets the log mode and log parameter information for a secondary resource manager (RM).
old-location: fs\fsctl_txfs_modify_rm.htm
tech.root: FileIO
ms.assetid: 29054321-a805-4a4e-90fb-a5b8e2858da0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_MODIFY_RM, FSCTL_TXFS_MODIFY_RM control, FSCTL_TXFS_MODIFY_RM control code [Files], base.fsctl_txfs_set_rm_information, fs.fsctl_txfs_modify_rm, fs.fsctl_txfs_set_rm_information, winioctl/FSCTL_TXFS_MODIFY_RM
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_TXFS_MODIFY_RM
dev_langs:
 - c++
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
- FSCTL_TXFS_MODIFY_RM
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_TXFS_MODIFY_RM IOCTL


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Sets the log mode and log parameter information for a secondary resource manager (RM).

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL
DeviceIoControl((HANDLE) hDevice,             // handle to device
                FSCTL_TXFS_MODIFY_RM,         // dwIoControlCode
                (LPVOID) lpInBuffer,          // input buffer
                (DWORD) nInBufferSize,        // size of input buffer
                NULL,                         // lpOutBuffer
                0,                            // nOutBufferSize
                (LPDWORD) lpBytesReturned,    // bytes returned
                (LPOVERLAPPED) lpOverlapped); // OVERLAPPED structure</pre>
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



<b>FSCTL_TXFS_MODIFY_RM</b> is a synchronous 
    operation.

This control code is for remote clients to use when setting log parameters, and for local clients to specify 
    log parameters for the default RMs.

<div class="alert"><b>Note</b>  You cannot set the logging mode for a default RM. The logging mode for a default RM is 
     <b>TXFS_LOGGING_MODE_SIMPLE</b>.</div>
<div> </div>
<b>ReFS:  </b>This code is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/transactional-ntfs-reference">Secondary Resource Managers for TxF Volumes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-txfs_modify_rm">TXFS_MODIFY_RM</a>
 

 

