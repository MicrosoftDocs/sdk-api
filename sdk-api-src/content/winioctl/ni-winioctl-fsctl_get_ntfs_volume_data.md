---
UID: NI:winioctl.FSCTL_GET_NTFS_VOLUME_DATA
title: FSCTL_GET_NTFS_VOLUME_DATA
description: Retrieves information about the specified NTFS file system volume.
old-location: fs\fsctl_get_ntfs_volume_data.htm
tech.root: FileIO
ms.assetid: b5690b4f-3967-41d8-bf11-70f8b1da79ad
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_NTFS_VOLUME_DATA, FSCTL_GET_NTFS_VOLUME_DATA control, FSCTL_GET_NTFS_VOLUME_DATA control code [Files], _win32_fsctl_get_ntfs_volume_data, base.fsctl_get_ntfs_volume_data, fs.fsctl_get_ntfs_volume_data, winioctl/FSCTL_GET_NTFS_VOLUME_DATA
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_GET_NTFS_VOLUME_DATA
dev_langs:
- c++
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
- FSCTL_GET_NTFS_VOLUME_DATA
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_GET_NTFS_VOLUME_DATA IOCTL


## -description


Retrieves information about the specified NTFS file system volume.

To perform this operation, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to device
  FSCTL_GET_NTFS_VOLUME_DATA, // dwIoControlCodeNULL,                       // lpInBuffer0,                          // nInBufferSize(LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
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



In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-ntfs_extended_volume_data">NTFS_VOLUME_DATA_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
 

 

