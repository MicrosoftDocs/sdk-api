---
UID: NI:winioctl.FSCTL_TXFS_GET_TRANSACTED_VERSION
title: FSCTL_TXFS_GET_TRANSACTED_VERSION
author: windows-sdk-content
description: Returns a TXFS_GET_TRANSACTED_VERSION structure. The structure identifies the most recently committed version of the specified file, the version number of the handle.
old-location: fs\fsctl_txfs_get_transacted_version.htm
tech.root: FileIO
ms.assetid: 71864348-1266-4ac5-a4b5-b9aaff52b0c5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_GET_TRANSACTED_VERSION, FSCTL_TXFS_GET_TRANSACTED_VERSION control, FSCTL_TXFS_GET_TRANSACTED_VERSION control code [Files], fs.fsctl_txfs_get_transacted_version, winioctl/FSCTL_TXFS_GET_TRANSACTED_VERSION
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
 - FSCTL_TXFS_GET_TRANSACTED_VERSION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_TXFS_GET_TRANSACTED_VERSION IOCTL


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Returns a <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_txfs_get_transacted_version">TXFS_GET_TRANSACTED_VERSION</a> structure.  The structure identifies the most recently committed version of the specified file, the version number of the handle. 

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
  FSCTL_TXFS_GET_TRANSACTED_VERSION, // dwIoControlCodeNULL,                          // lpInBuffer0,                             // nInBufferSize(LPVOID) lpOutBuffer,          // output buffer
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



<b>FSCTL_TXFS_GET_TRANSACTED_VERSION</b> is 
    a synchronous operation.

This control code can be use to track the latest version of a base file. For a specified handle, the base 
    version is always the base value returned when the handle was opened, but the latest version changes based on any 
    commit operations another transaction makes.  If handle is then closed and opened again, base version and latest 
    version are updated to new values and any subsequent commit operations from the other transaction  change the 
    latest version.

If you attempt to retrieve the version of a resource manager's root, the value 
    <b>TXFS_TRANSACTED_VERSION_NONTRANSACTED</b> is returned.

<b>ReFS:  </b>This code is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_txfs_get_transacted_version">TXFS_GET_TRANSACTED_VERSION</a>
 

 

