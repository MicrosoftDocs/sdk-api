---
UID: NI:winioctl.FSCTL_TXFS_WRITE_BACKUP_INFORMATION
title: FSCTL_TXFS_WRITE_BACKUP_INFORMATION

description: Writes Transactional NTFS (TxF) specific information to a specified file.
old-location: fs\fsctl_txfs_write_backup_information.htm
tech.root: FileIO
ms.assetid: 36080d53-9004-40f7-9d92-c6deaac8299f

ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_WRITE_BACKUP_INFORMATION, FSCTL_TXFS_WRITE_BACKUP_INFORMATION control, FSCTL_TXFS_WRITE_BACKUP_INFORMATION control code [Files], fs.fsctl_txfs_write_backup_information, winioctl/FSCTL_TXFS_WRITE_BACKUP_INFORMATION
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_TXFS_WRITE_BACKUP_INFORMATION
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
- FSCTL_TXFS_WRITE_BACKUP_INFORMATION
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_TXFS_WRITE_BACKUP_INFORMATION IOCTL


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Writes  Transactional NTFS (TxF) specific information to a specified file. The 
    <b>Buffer</b> member of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-txfs_write_backup_information">TXFS_WRITE_BACKUP_INFORMATION</a> structure must 
    be the <b>Buffer</b> member of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-txfs_read_backup_information_out">TXFS_READ_BACKUP_INFORMATION_OUT</a> 
    structure returned by 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_read_backup_information">FSCTL_TXFS_READ_BACKUP_INFORMATION</a>.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to device
  FSCTL_TXFS_WRITE_BACKUP_INFORMATION, // dwIoControlCode(LPVOID) lpInBuffer,           // input buffer
  (DWORD) nInBufferSize,         // size of input buffer
  NULL,                          // lpOutBuffer0,                             // nOutBufferSize(LPDWORD) lpBytesReturned,     // number of bytes returned
  NULL                           // OVERLAPPED structure
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



<b>FSCTL_TXFS_WRITE_BACKUP_INFORMATION</b> 
    is a synchronous operation.

This control code can be used by backup functions and applications, such as 
    Win32 <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-backupread">BackupRead</a>, and by Volume Snapshot Service (VSS) 
    writers that support secondary resource managers. For more information, see 
    <a href="https://docs.microsoft.com/windows-server/storage/file-server/volume-shadow-copy-service">Volume Shadow Copy Service</a>.

<b>ReFS:  </b>This code is not supported.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_txfs_read_backup_information">FSCTL_TXFS_READ_BACKUP_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-txfs_write_backup_information">TXFS_WRITE_BACKUP_INFORMATION</a>



<a href="https://docs.microsoft.com/windows-server/storage/file-server/volume-shadow-copy-service">Volume Shadow Copy Service</a>
 

 

