---
UID: NI:winioctl.IOCTL_VOLUME_IS_CLUSTERED
title: IOCTL_VOLUME_IS_CLUSTERED
description: Determines whether the specified volume is clustered.
helpviewer_keywords: ["IOCTL_VOLUME_IS_CLUSTERED","IOCTL_VOLUME_IS_CLUSTERED control","IOCTL_VOLUME_IS_CLUSTERED control code [Files]","_win32_ioctl_volume_is_clustered","base.ioctl_volume_is_clustered","fs.ioctl_volume_is_clustered","winioctl/IOCTL_VOLUME_IS_CLUSTERED"]
old-location: fs\ioctl_volume_is_clustered.htm
tech.root: fs
ms.assetid: 3722b08c-237d-4551-b75e-1d28fe8e94c3
ms.date: 12/05/2018
ms.keywords: IOCTL_VOLUME_IS_CLUSTERED, IOCTL_VOLUME_IS_CLUSTERED control, IOCTL_VOLUME_IS_CLUSTERED control code [Files], _win32_ioctl_volume_is_clustered, base.ioctl_volume_is_clustered, fs.ioctl_volume_is_clustered, winioctl/IOCTL_VOLUME_IS_CLUSTERED
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IOCTL_VOLUME_IS_CLUSTERED
 - winioctl/IOCTL_VOLUME_IS_CLUSTERED
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
 - IOCTL_VOLUME_IS_CLUSTERED
---

# IOCTL_VOLUME_IS_CLUSTERED IOCTL


## -description

Determines whether the specified volume is clustered.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_VOLUME_IS_CLUSTERED,    // dwIoControlCode
  NULL,                         // lpInBuffer
  0,                            // nInBufferSize
  NULL,                         // lpOutBuffer
  0,                            // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
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

The **IOCTL_VOLUME_IS_CLUSTERED** control code is valid only if the Cluster service is running.

The **ERROR_GEN_FAILURE** error indicates that the computer that currently owns the disk on which the volume resides is a server cluster node, but either the disk is a Physical Disk resource currently in an offline state or the disk is not a Physical Disk resource. To determine which of these situations exists, use the following steps:

1. Call the [ClusterEnum](../clusapi/nf-clusapi-clusterenum.md) function to enumerate all Physical Disk resources in the cluster.
1. Search each enumerated Physical Disk resource for the volume by calling the [ClusterResourceControl](../clusapi/nf-clusapi-clusterresourcecontrol.md) function with [CLUSCTL_RESOURCE_STORAGE_GET_DISK_INFO](/previous-versions/windows/desktop/mscs/clusctl-resource-storage-get-disk-info). If you cannot find the volume among the Physical Disk resources in the cluster, the volume does not reside on a Physical Disk resource.

The **ERROR_INVALID_FUNCTION** error indicates that the computer that currently owns the disk on which the volume resides is not a server cluster node or the disk is not a Physical Disk resource. To determine whether a computer is a server cluster node, call the [GetNodeClusterState](../clusapi/nf-clusapi-getnodeclusterstate.md) function.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)