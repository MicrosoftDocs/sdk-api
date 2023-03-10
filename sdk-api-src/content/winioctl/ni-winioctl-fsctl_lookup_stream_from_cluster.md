---
UID: NI:winioctl.FSCTL_LOOKUP_STREAM_FROM_CLUSTER
title: FSCTL_LOOKUP_STREAM_FROM_CLUSTER
description: Given a handle to a NTFS volume or a file on a NTFS volume, returns a chain of data structures that describes streams that occupy the specified clusters.
helpviewer_keywords: ["FSCTL_LOOKUP_STREAM_FROM_CLUSTER","FSCTL_LOOKUP_STREAM_FROM_CLUSTER control","FSCTL_LOOKUP_STREAM_FROM_CLUSTER control code [Files]","fs.fsctl_lookup_stream_from_cluster","winioctl/FSCTL_LOOKUP_STREAM_FROM_CLUSTER"]
old-location: fs\fsctl_lookup_stream_from_cluster.htm
tech.root: fs
ms.assetid: 21a7cad2-eae0-461d-802e-a54fd7d35808
ms.date: 12/05/2018
ms.keywords: FSCTL_LOOKUP_STREAM_FROM_CLUSTER, FSCTL_LOOKUP_STREAM_FROM_CLUSTER control, FSCTL_LOOKUP_STREAM_FROM_CLUSTER control code [Files], fs.fsctl_lookup_stream_from_cluster, winioctl/FSCTL_LOOKUP_STREAM_FROM_CLUSTER
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - FSCTL_LOOKUP_STREAM_FROM_CLUSTER
 - winioctl/FSCTL_LOOKUP_STREAM_FROM_CLUSTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FSCTL_LOOKUP_STREAM_FROM_CLUSTER
---

# FSCTL_LOOKUP_STREAM_FROM_CLUSTER IOCTL


## -description

Given a handle to a NTFS volume or a file on a NTFS volume, returns a chain of data structures that describes streams that occupy the specified clusters.

> [!IMPORTANT]
> **FSCTL_LOOKUP_STREAM_FROM_CLUSTER** is a very resource-intensive operation, and typically uses a very large amount of disk bandwidth, memory, and time. It is unlikely that much of this information will remain in cache so a second call to **FSCTL_LOOKUP_STREAM_FROM_CLUSTER** would take nearly as much time as the first call. For doing multiple lookups it's more efficient to use [FSCTL_ENUM_USN_DATA](ni-winioctl-fsctl_enum_usn_data.md) to enumerate every MFT record and then use [FSCTL_GET_RETRIEVAL_POINTERS](ni-winioctl-fsctl_get_retrieval_pointers.md) to gather the data to map between clusters and streams.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE)       hDevice,               // handle to file, directory, or volume
  FSCTL_LOOKUP_STREAM_FROM_CLUSTER,     // dwIoControlCode
  (LPVOID)       lpInBuffer,            // input buffer
  (DWORD)        nInBufferSize,         // size of input buffer
  (LPVOID)       lpOutBuffer,           // output buffer
  (DWORD)        nOutBufferSize,        // size of output buffer
  (LPDWORD)      lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped           // OVERLAPPED structure
);
```

## -ioctlparameters

### -input-buffer

### -input-buffer-length

### -output-buffer

### -output-buffer-length

### -in-out-buffer

### -inout-buffer-length

### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [Defragmentation](/windows/desktop/FileIO/defragmenting-files)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md)
* [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md)
* [GetQueuedCompletionStatus](../ioapiset/nf-ioapiset-getqueuedcompletionstatus.md)
* [LOOKUP_STREAM_FROM_CLUSTER_ENTRY](ns-winioctl-lookup_stream_from_cluster_entry.md)
* [LOOKUP_STREAM_FROM_CLUSTER_INPUT](ns-winioctl-lookup_stream_from_cluster_input.md)
* [LOOKUP_STREAM_FROM_CLUSTER_OUTPUT](ns-winioctl-lookup_stream_from_cluster_output.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)