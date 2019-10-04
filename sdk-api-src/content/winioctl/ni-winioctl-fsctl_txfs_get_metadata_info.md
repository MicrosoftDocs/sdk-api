---
UID: NI:winioctl.FSCTL_TXFS_GET_METADATA_INFO
title: FSCTL_TXFS_GET_METADATA_INFO
author: windows-sdk-content
description: Retrieves Transacted NTFS (TxF) metadata for a file and the GUID of the transaction that has locked the specified file (if the file is locked).
old-location: fs\fsctl_txfs_get_metadata_info.htm
tech.root: FileIO
ms.assetid: 129e682c-bc95-46d5-a0d3-adbadc7e6478
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_GET_METADATA_INFO, FSCTL_TXFS_GET_METADATA_INFO control, FSCTL_TXFS_GET_METADATA_INFO control code [Files], fs.fsctl_txfs_get_metadata_info, winioctl/FSCTL_TXFS_GET_METADATA_INFO
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_TXFS_GET_METADATA_INFO
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
- FSCTL_TXFS_GET_METADATA_INFO
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_TXFS_GET_METADATA_INFO IOCTL


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Retrieves Transacted NTFS (TxF) metadata for a file and the <b>GUID</b> of the transaction that has locked the specified file (if the file is locked). 

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to device
  FSCTL_TXFS_GET_METADATA_INFO, // dwIoControlCodeNULL,                          // lpInBuffer0,                             // nInBufferSize(LPVOID) lpOutBuffer,          // output buffer
  (DWORD) nOutBufferSize,        // size of output buffer
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  NULL    // OVERLAPPED structure
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



<b>FSCTL_TXFS_GET_METADATA_INFO</b> is a 
    synchronous operation.

<b>ReFS:  </b>This code is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-txfs_get_metadata_info_out">TXFS_GET_METADATA_INFO_OUT</a>
 

 

