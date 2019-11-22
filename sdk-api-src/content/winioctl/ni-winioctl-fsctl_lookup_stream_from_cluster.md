---
UID: NI:winioctl.FSCTL_LOOKUP_STREAM_FROM_CLUSTER
title: FSCTL_LOOKUP_STREAM_FROM_CLUSTER

description: Given a handle to a NTFS volume or a file on a NTFS volume, returns a chain of data structures that describes streams that occupy the specified clusters.
old-location: fs\fsctl_lookup_stream_from_cluster.htm
tech.root: FileIO
ms.assetid: 21a7cad2-eae0-461d-802e-a54fd7d35808

ms.date: 12/05/2018
ms.keywords: FSCTL_LOOKUP_STREAM_FROM_CLUSTER, FSCTL_LOOKUP_STREAM_FROM_CLUSTER control, FSCTL_LOOKUP_STREAM_FROM_CLUSTER control code [Files], fs.fsctl_lookup_stream_from_cluster, winioctl/FSCTL_LOOKUP_STREAM_FROM_CLUSTER
ms.topic: ioctl
f1_keywords:
- winioctl/FSCTL_LOOKUP_STREAM_FROM_CLUSTER
dev_langs:
 - c++
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
- FSCTL_LOOKUP_STREAM_FROM_CLUSTER
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_LOOKUP_STREAM_FROM_CLUSTER IOCTL


## -description


Given a handle to a NTFS volume or a file on a NTFS volume, returns a chain of data structures that 
    describes streams that occupy the specified clusters.
<div class="alert"><b>Important</b>  <b>FSCTL_LOOKUP_STREAM_FROM_CLUSTER</b> 
    is a very resource-intensive operation, and typically uses a very large amount of disk bandwidth, memory, and time. It is 
    unlikely that much of this information will remain in cache so a second call to 
    <b>FSCTL_LOOKUP_STREAM_FROM_CLUSTER</b> would 
    take nearly as much time as the first call. For doing multiple lookups it's more efficient to use 
    <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_enum_usn_data">FSCTL_ENUM_USN_DATA</a> to enumerate every MFT record and 
    then use <a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers">FSCTL_GET_RETRIEVAL_POINTERS</a> to 
    gather the data to map between clusters and streams.</div><div> </div>To perform this operation, call the <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
   function with the following parameters.
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DeviceIoControl( (HANDLE)       hDevice,           // handle to file, directory, or volume 
                 FSCTL_LOOKUP_STREAM_FROM_CLUSTER, // dwIoControlCode(LPVOID)       lpInBuffer,        // input buffer 
                 (DWORD)        nInBufferSize,     // size of input buffer 
                 (LPVOID)       lpOutBuffer,       // output buffer 
                 (DWORD)        nOutBufferSize,    // size of output buffer 
                 (LPDWORD)      lpBytesReturned,   // number of bytes returned 
                 (LPOVERLAPPED) lpOverlapped );    // OVERLAPPED structure</pre>
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




<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/defragmenting-files">Defragmentation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/disk-management-control-codes">Disk Management Control Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-lookup_stream_from_cluster_entry">LOOKUP_STREAM_FROM_CLUSTER_ENTRY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-lookup_stream_from_cluster_input">LOOKUP_STREAM_FROM_CLUSTER_INPUT</a>



<a href="https://docs.microsoft.com/windows/win32/api/winioctl/ns-winioctl-lookup_stream_from_cluster_output">LOOKUP_STREAM_FROM_CLUSTER_OUTPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>
 

 

