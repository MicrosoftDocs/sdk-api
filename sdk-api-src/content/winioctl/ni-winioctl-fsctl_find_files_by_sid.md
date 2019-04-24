---
UID: NI:winioctl.FSCTL_FIND_FILES_BY_SID
title: FSCTL_FIND_FILES_BY_SID
author: windows-sdk-content
description: Searches a directory for a file whose creator owner matches the specified SID.
old-location: fs\fsctl_find_files_by_sid.htm
tech.root: FileIO
ms.assetid: 10d46c2e-9403-4c8a-8847-f427fbc6c905
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_FIND_FILES_BY_SID, FSCTL_FIND_FILES_BY_SID control, FSCTL_FIND_FILES_BY_SID control code [Files], base.fsctl_find_files_by_sid, fs.fsctl_find_files_by_sid, winioctl/FSCTL_FIND_FILES_BY_SID
ms.topic: ioctl
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
 - FSCTL_FIND_FILES_BY_SID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_FIND_FILES_BY_SID IOCTL


## -description


Searches a directory for a file whose creator owner matches the specified SID.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl(
  (HANDLE) hDevice,            // handle to volume
  FSCTL_FIND_FILES_BY_SID,     // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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



This control code requires the use of <a href="https://msdn.microsoft.com/42efbd5b-6455-4319-a76e-cdb666fc36b8">disk quotas</a> on 
     the volume.

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
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

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




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/fd0294a1-be43-4353-8edc-dff8bf0b0787">FIND_BY_SID_DATA</a>



<a href="https://msdn.microsoft.com/fc616f88-c8c9-43de-8b17-2b8c38e5cdbb">FIND_BY_SID_OUTPUT</a>



<a href="https://msdn.microsoft.com/e27ded4b-d104-4244-b38e-5fed10d32e1e">File  Management Control Codes</a>
 

 

