---
UID: NI:winioctl.FSCTL_GET_BOOT_AREA_INFO
title: FSCTL_GET_BOOT_AREA_INFO
author: windows-sdk-content
description: Retrieves the locations of boot sectors for a volume.
old-location: fs\fsctl_get_boot_area_info.htm
tech.root: FileIO
ms.assetid: 5739354b-5342-4be9-ac50-bb983d51587c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_BOOT_AREA_INFO, FSCTL_GET_BOOT_AREA_INFO control, FSCTL_GET_BOOT_AREA_INFO control code [Files], fs.fsctl_get_boot_area_info, winioctl/FSCTL_GET_BOOT_AREA_INFO
ms.topic: ioctl
f1_keywords: ["winioctl/FSCTL_GET_BOOT_AREA_INFO"]
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
 - FSCTL_GET_BOOT_AREA_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_GET_BOOT_AREA_INFO IOCTL


## -description


Retrieves the locations of boot sectors for a volume. 

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
  (HANDLE) hDevice,              // handle to volume
  FSCTL_GET_BOOT_AREA_INFO,      // dwIoControlCode(LPVOID) NULL,                 // input buffer
  (DWORD) 0,                     // size of input buffer
  (LPVOID) lpOutBuffer,          // output buffer
  (DWORD) nOutBufferSize,        // size of output buffer
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
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



<a href="https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes">Volume Management Control Codes</a>
 

 

