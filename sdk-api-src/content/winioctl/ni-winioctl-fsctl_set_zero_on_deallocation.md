---
UID: NI:winioctl.FSCTL_SET_ZERO_ON_DEALLOCATION
title: FSCTL_SET_ZERO_ON_DEALLOCATION
description: Indicates an NTFS file system file handle should have its clusters filled with zeros when it is deallocated.helpviewer_keywords: ["FSCTL_SET_ZERO_ON_DEALLOCATION","FSCTL_SET_ZERO_ON_DEALLOCATION control","FSCTL_SET_ZERO_ON_DEALLOCATION control code [Files]","fs.fsctl_set_zero_on_deallocation","winioctl/FSCTL_SET_ZERO_ON_DEALLOCATION"]
old-location: fs\fsctl_set_zero_on_deallocation.htm
tech.root: FileIO
ms.assetid: dc926f24-de52-431b-bac2-f97535de6848
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_ZERO_ON_DEALLOCATION, FSCTL_SET_ZERO_ON_DEALLOCATION control, FSCTL_SET_ZERO_ON_DEALLOCATION control code [Files], fs.fsctl_set_zero_on_deallocation, winioctl/FSCTL_SET_ZERO_ON_DEALLOCATION
f1_keywords:
- winioctl/FSCTL_SET_ZERO_ON_DEALLOCATION
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
- FSCTL_SET_ZERO_ON_DEALLOCATION
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SET_ZERO_ON_DEALLOCATION IOCTL


## -description


Indicates an NTFS file system file handle should have its clusters filled with zeros when it is 
    deallocated. If a file is resident, it is converted to nonresident. When clusters are deallocated, the 
    clusters on a disk are zeroed.  If a file is deleted, all clusters associated with the file are zeroed.

To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,               // handle to device
                 FSCTL_SET_ZERO_ON_DEALLOCATION, // dwIoControlCodeNULL,                           // lpInBuffer0,                              // nInBufferSizeNULL,                           // lpOutBuffer0,                              // nOutBufferSize(LPDWORD) lpBytesReturned,      // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>
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




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>
 

 

