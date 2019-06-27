---
UID: NI:winioctl.FSCTL_SET_REPAIR
title: FSCTL_SET_REPAIR
author: windows-sdk-content
description: Sets the mode of an NTFS file system's self-healing capability.
old-location: fs\fsctl_set_repair.htm
tech.root: FileIO
ms.assetid: 3df03a87-7117-4f85-a04e-54bcd800e8ff
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_REPAIR, FSCTL_SET_REPAIR control, FSCTL_SET_REPAIR control code [Files], SET_REPAIR_DELETE_CROSSLINK, SET_REPAIR_DISABLED_AND_BUGCHECK_ON_CORRUPT, SET_REPAIR_ENABLED, SET_REPAIR_VOLUME_BITMAP_SCAN, SET_REPAIR_WARN_ABOUT_DATA_LOSS, fs.fsctl_set_repair, winioctl/FSCTL_SET_REPAIR
ms.topic: ioctl
f1_keywords: 
 - "winioctl/FSCTL_SET_REPAIR"
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
 - FSCTL_SET_REPAIR
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SET_REPAIR IOCTL


## -description


Sets the mode of an NTFS file system's self-healing capability.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL WINAPI DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_SET_REPAIR,             // dwIoControlCode(PUSHORT) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  NULL,                         // not used
  0,                            // not used
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
No

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_repair">FSCTL_GET_REPAIR</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_initiate_repair">FSCTL_INITIATE_REPAIR</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_wait_for_repair">FSCTL_WAIT_FOR_REPAIR</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>
 

 

