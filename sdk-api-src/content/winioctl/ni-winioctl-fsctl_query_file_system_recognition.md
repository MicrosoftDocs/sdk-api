---
UID: NI:winioctl.FSCTL_QUERY_FILE_SYSTEM_RECOGNITION
title: FSCTL_QUERY_FILE_SYSTEM_RECOGNITION
author: windows-sdk-content
description: Queries for file system recognition information on a volume.
old-location: fs\fsctl_query_file_system_recognition.htm
tech.root: FileIO
ms.assetid: 0b2ff131-a659-4bd0-b329-41fb60edbe13
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_FILE_SYSTEM_RECOGNITION, FSCTL_QUERY_FILE_SYSTEM_RECOGNITION control, FSCTL_QUERY_FILE_SYSTEM_RECOGNITION control code [Files], fs.fsctl_query_file_system_recognition, winioctl/FSCTL_QUERY_FILE_SYSTEM_RECOGNITION
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - FSCTL_QUERY_FILE_SYSTEM_RECOGNITION
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_QUERY_FILE_SYSTEM_RECOGNITION IOCTL


## -description


Queries for file system recognition information on a volume.

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
  (HANDLE) hDevice,             // handle to volume
  FSCTL_QUERY_FILE_SYSTEM_RECOGNITION, // dwIoControlCodeNULL,                         // lpInBuffer0,                            // nInBufferSize(LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
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
No

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_file_system_recognition_information">FILE_SYSTEM_RECOGNITION_INFORMATION</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-system-recognition-structure">FILE_SYSTEM_RECOGNITION_STRUCTURE</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-system-recognition">File System Recognition</a>
 

 

