---
UID: NI:winioctl.FSCTL_MAKE_MEDIA_COMPATIBLE
title: FSCTL_MAKE_MEDIA_COMPATIBLE
description: Closes an open UDF session on write-once media to make the media ROM compatible.helpviewer_keywords: ["FSCTL_MAKE_MEDIA_COMPATIBLE","FSCTL_MAKE_MEDIA_COMPATIBLE control","FSCTL_MAKE_MEDIA_COMPATIBLE control code [Files]","fs.fsctl_make_media_compatible","winioctl/FSCTL_MAKE_MEDIA_COMPATIBLE"]
old-location: fs\fsctl_make_media_compatible.htm
tech.root: FileIO
ms.assetid: bbe58c35-d0da-4c29-a412-a84a138dc9fb
ms.date: 12/05/2018
ms.keywords: FSCTL_MAKE_MEDIA_COMPATIBLE, FSCTL_MAKE_MEDIA_COMPATIBLE control, FSCTL_MAKE_MEDIA_COMPATIBLE control code [Files], fs.fsctl_make_media_compatible, winioctl/FSCTL_MAKE_MEDIA_COMPATIBLE
f1_keywords:
- winioctl/FSCTL_MAKE_MEDIA_COMPATIBLE
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
- FSCTL_MAKE_MEDIA_COMPATIBLE
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_MAKE_MEDIA_COMPATIBLE IOCTL


## -description


Closes an open UDF session on write-once media to make the media ROM compatible. Used in conjunction with <b>FILE_SEQUENTIAL_WRITE_ONCE</b> volume flag. This call must be issued on the volume handle.

To perform this operation, call the 
   <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_MAKE_MEDIA_COMPATIBLE, // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  NULL,                        // output buffer
  0,                           // size of output buffer
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).




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
No

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



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-file_make_compatible_buffer">FILE_MAKE_COMPATIBLE_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>
 

 

