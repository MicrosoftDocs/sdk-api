---
UID: NI:winioctl.FSCTL_LOOKUP_STREAM_FROM_CLUSTER
title: FSCTL_LOOKUP_STREAM_FROM_CLUSTER
author: windows-sdk-content
description: Given a handle to a NTFS volume or a file on a NTFS volume, returns a chain of data structures that describes streams that occupy the specified clusters.
old-location: fs\fsctl_lookup_stream_from_cluster.htm
tech.root: FileIO
ms.assetid: 21a7cad2-eae0-461d-802e-a54fd7d35808
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FSCTL_LOOKUP_STREAM_FROM_CLUSTER, FSCTL_LOOKUP_STREAM_FROM_CLUSTER control, FSCTL_LOOKUP_STREAM_FROM_CLUSTER control code [Files], fs.fsctl_lookup_stream_from_cluster, winioctl/FSCTL_LOOKUP_STREAM_FROM_CLUSTER
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
 - FSCTL_LOOKUP_STREAM_FROM_CLUSTER
product: Windows
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
    <a href="https://msdn.microsoft.com/44d20401-a2ed-4756-9fda-878a24eab7c3">FSCTL_ENUM_USN_DATA</a> to enumerate every MFT record and 
    then use <a href="https://msdn.microsoft.com/002f6703-8db3-4034-a79f-3fa9c4159115">FSCTL_GET_RETRIEVAL_POINTERS</a> to 
    gather the data to map between clusters and streams.</div><div> </div>To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
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




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/27ccaab7-ec89-489b-80dc-df9beb7969bc">Defragmentation</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/488a7d32-cbb5-4f32-9655-0aca8ac69640">Disk Management Control Codes</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>



<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>



<a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>



<a href="https://msdn.microsoft.com/2f4de631-8bb4-4b2a-a750-43f06554b22f">LOOKUP_STREAM_FROM_CLUSTER_ENTRY</a>



<a href="https://msdn.microsoft.com/4b398ae8-a396-4917-bcb8-aa5f5920296f">LOOKUP_STREAM_FROM_CLUSTER_INPUT</a>



<a href="https://msdn.microsoft.com/1e9b99eb-93a8-4f0c-98ee-ca9f58466400">LOOKUP_STREAM_FROM_CLUSTER_OUTPUT</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

