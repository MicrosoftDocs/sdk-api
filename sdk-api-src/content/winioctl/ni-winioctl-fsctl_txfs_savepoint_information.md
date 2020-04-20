---
UID: NI:winioctl.FSCTL_TXFS_SAVEPOINT_INFORMATION
title: FSCTL_TXFS_SAVEPOINT_INFORMATION
description: The FSCTL_TXFS_SAVEPOINT_INFORMATION control code controls setting, clearing, and rolling back to the specified savepoint.helpviewer_keywords: ["FSCTL_TXFS_SAVEPOINT_INFORMATION","FSCTL_TXFS_SAVEPOINT_INFORMATION control","FSCTL_TXFS_SAVEPOINT_INFORMATION control code [Files]","fs.fsctl_txfs_savepoint_information","winioctl/FSCTL_TXFS_SAVEPOINT_INFORMATION"]
old-location: fs\fsctl_txfs_savepoint_information.htm
tech.root: FileIO
ms.assetid: 50cf01b4-fd14-4468-9191-79ccd0e2bd05
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_SAVEPOINT_INFORMATION, FSCTL_TXFS_SAVEPOINT_INFORMATION control, FSCTL_TXFS_SAVEPOINT_INFORMATION control code [Files], fs.fsctl_txfs_savepoint_information, winioctl/FSCTL_TXFS_SAVEPOINT_INFORMATION
f1_keywords:
- winioctl/FSCTL_TXFS_SAVEPOINT_INFORMATION
dev_langs:
- c++
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
- FSCTL_TXFS_SAVEPOINT_INFORMATION
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_TXFS_SAVEPOINT_INFORMATION IOCTL


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

The <b>FSCTL_TXFS_SAVEPOINT_INFORMATION</b> 
   control code controls setting, clearing, and rolling back to the specified savepoint.

To perform this operation, call the 
   <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
DeviceIoControl(
  (HANDLE) hDevice,                 // handle to resource manager
  FSCTL_TXFS_SAVEPOINT_INFORMATION, // dwIoControlCode
  (LPVOID)lpInBuffer ,              // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
  (LPVOID) lpOutBuffer,             // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
  (LPDWORD) lpBytesReturned,        // number of bytes returned
  (LPOVERLAPPED) lpOverlapped );    // OVERLAPPED structure</pre>
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




## -remarks



<b>ReFS:  </b>This code is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-txfs_savepoint_information">TXFS_SAVEPOINT_INFORMATION</a>
 

 

