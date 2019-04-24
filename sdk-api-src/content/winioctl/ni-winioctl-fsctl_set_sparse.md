---
UID: NI:winioctl.FSCTL_SET_SPARSE
title: FSCTL_SET_SPARSE
author: windows-sdk-content
description: Marks the indicated file as sparse or not sparse. In a sparse file, large ranges of zeros may not require disk allocation.
old-location: fs\fsctl_set_sparse.htm
tech.root: FileIO
ms.assetid: aa8f5880-f831-49b6-8359-fe07c78c032f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_SPARSE, FSCTL_SET_SPARSE control, FSCTL_SET_SPARSE control code [Files], _win32_fsctl_set_sparse, base.fsctl_set_sparse, fs.fsctl_set_sparse, winioctl/FSCTL_SET_SPARSE
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
 - FSCTL_SET_SPARSE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_SET_SPARSE IOCTL


## -description


Marks the indicated file as sparse or  not sparse. In a sparse file, large ranges of zeros may not 
    require disk allocation. Space for nonzero data will be allocated as needed as the file is written.

To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
    function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BOOL DeviceIoControl( (HANDLE) hDevice,                     // handle to a file
                      FSCTL_SET_SPARSE,                     // dwIoControlCode(PFILE_SET_SPARSE_BUFFER) lpInBuffer, // input buffer
                      (DWORD) nInBufferSize,                // size of input buffer
                      NULL,                                 // lpOutBuffer0,                                    // nOutBufferSize(LPDWORD) lpBytesReturned,            // number of bytes returned
                      (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure</pre>
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



For the implications of overlapped I/O on this operation, see the Remarks section of 
    <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>.

The <b>FSCTL_SET_SPARSE</b> control code sets or clears the 
    <b>FILE_ATTRIBUTE_SPARSE_FILE</b> attribute of the specified file.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>A clear operation is valid only on files that no longer have any sparse regions. Performing a clear 
      operation on a file with sparse regions can have unpredictable results.

 
    You can determine whether there are any sparse regions in a file by using the 
    <a href="https://msdn.microsoft.com/053e26ec-1529-41b3-aeb6-128b3085bafc">FSCTL_QUERY_ALLOCATED_RANGES</a> control 
    code.

If the <i>lpInBuffer</i> parameter is <b>NULL</b>, the operation will 
     behave the same as if the <b>SetSparse</b> member of the 
     <a href="https://msdn.microsoft.com/f9c24156-bcd6-423e-b055-18651f4e185e">FILE_SET_SPARSE_BUFFER</a> structure were 
     <b>TRUE</b>. In other words, the operation sets the file to a sparse file.

<b>Windows Server 2003 and Windows XP:  </b>If a <a href="https://msdn.microsoft.com/f9c24156-bcd6-423e-b055-18651f4e185e">FILE_SET_SPARSE_BUFFER</a> structure is 
      passed in the <i>lpInBuffer</i> parameter, the only valid value for the 
      <b>SetSparse</b> member is <b>TRUE</b>, which sets the file to a sparse 
      file. Passing <b>FALSE</b> in the 
      <b>FILE_SET_SPARSE_BUFFER</b> structure will cause this 
      function call to fail. The only way to clear this attribute is to overwrite the file (for example, by calling 
      the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function with the 
      <b>CREATE_ALWAYS</b> flag).

You cannot create a sparse file by calling 
    <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> with 
    <b>FILE_ATTRIBUTE_SPARSE_FILE</b> in the <i>dwFlagsAndAttributes</i> 
    parameter. You must use the <b>FSCTL_SET_SPARSE</b> control 
    code.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use 
    unbuffered I/O.

In Windows 8 and Windows Server 2012, this code is supported by the following 
    technologies.

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
See Comment

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
 

CsvFs will do redirected IO for sparse files. CsvFs allows making file sparse only when the file is opened 
     exclusively by a node. SMB 3.0 Transparent Failover does not support buffered write."




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/f9c24156-bcd6-423e-b055-18651f4e185e">FILE_SET_SPARSE_BUFFER</a>



<a href="https://msdn.microsoft.com/053e26ec-1529-41b3-aeb6-128b3085bafc">FSCTL_QUERY_ALLOCATED_RANGES</a>



<a href="https://msdn.microsoft.com/ee32f836-682e-4c26-b7d6-82e3b7b234f9">FSCTL_SET_ZERO_DATA</a>



<a href="https://msdn.microsoft.com/e27ded4b-d104-4244-b38e-5fed10d32e1e">File Management Control Codes</a>



<a href="https://msdn.microsoft.com/7326041d-f11e-4b80-ac4e-07173e418ce7">Sparse Files</a>
 

 

