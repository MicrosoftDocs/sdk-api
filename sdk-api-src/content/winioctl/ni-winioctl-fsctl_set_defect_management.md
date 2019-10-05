---
UID: NI:winioctl.FSCTL_SET_DEFECT_MANAGEMENT
title: FSCTL_SET_DEFECT_MANAGEMENT
author: windows-sdk-content
description: Sets the software defect management state for the specified file. Used for UDF file systems.
old-location: fs\fsctl_set_defect_management.htm
tech.root: FileIO
ms.assetid: 6febbce3-7e70-43c1-a75e-84addc218857
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_DEFECT_MANAGEMENT, FSCTL_SET_DEFECT_MANAGEMENT control, FSCTL_SET_DEFECT_MANAGEMENT control code [Files], fs.fsctl_set_defect_management, winioctl/FSCTL_SET_DEFECT_MANAGEMENT
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_SET_DEFECT_MANAGEMENT
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
- FSCTL_SET_DEFECT_MANAGEMENT
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SET_DEFECT_MANAGEMENT IOCTL


## -description


Sets the software defect management state for the specified file. Used for UDF file systems.

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
  FSCTL_SET_DEFECT_MANAGEMENT, // dwIoControlCode(LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  NULL,                        // output buffer
  0,                           // output buffer size
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



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-file_set_defect_mgmt_buffer">FILE_SET_DEFECT_MGMT_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>
 

 

