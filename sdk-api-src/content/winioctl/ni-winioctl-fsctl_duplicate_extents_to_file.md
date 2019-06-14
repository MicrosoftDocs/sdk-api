---
UID: NI:winioctl.FSCTL_DUPLICATE_EXTENTS_TO_FILE
title: FSCTL_DUPLICATE_EXTENTS_TO_FILE
author: windows-sdk-content
description: Instructs the file system to copy a range of file bytes on behalf of an application.
old-location: fs\fsctl_duplicate_extents_to_file.htm
tech.root: FileIO
ms.assetid: D66D2172-9308-4138-A321-867589787FED
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_DUPLICATE_EXTENTS_TO_FILE, FSCTL_DUPLICATE_EXTENTS_TO_FILE control, FSCTL_DUPLICATE_EXTENTS_TO_FILE control code [Files], fs.fsctl_duplicate_extents_to_file, winioctl/FSCTL_DUPLICATE_EXTENTS_TO_FILE
ms.topic: ioctl
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - FSCTL_DUPLICATE_EXTENTS_TO_FILE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_DUPLICATE_EXTENTS_TO_FILE IOCTL


## -description


Instructs the file system to copy a range of file bytes on behalf of an application. The destination file may be the same as, or different from, the source file. See <a href="https://docs.microsoft.com/windows/desktop/FileIO/block-cloning">Block Cloning</a> for more information.

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
   DeviceIoControl( (HANDLE)       hDevice,          // handle to device
                    FSCTL_DUPLICATE_EXTENTS_TO_FILE, // dwIoControlCode(LPVOID)       lpInBuffer,       // input buffer
                    (DWORD)        nInBufferSize,    // size of input buffer
                    NULL,                            // lpOutBuffer0,                               // nOutBufferSize(LPDWORD)      lpBytesReturned,  // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );   // OVERLAPPED structure</pre>
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



  For the implications of overlapped I/O on this operation, see the Remarks section of the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> topic.

See <a href="https://docs.microsoft.com/windows/desktop/FileIO/block-cloning">Block Cloning</a> for more information on this operation.

In Windows Server 2016, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.1.1 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.1.1 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.1.1 with Scale-out File Shares (SoFS)

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
Yes

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/block-cloning">Block Cloning</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_duplicate_extents_data">DUPLICATE_EXTENTS_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>
 

 

