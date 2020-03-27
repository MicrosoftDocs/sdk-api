---
UID: NI:winioctl.FSCTL_ALLOW_EXTENDED_DASD_IO
title: FSCTL_ALLOW_EXTENDED_DASD_IO
description: Signals the file system driver not to perform any I/O boundary checks on partition read or write calls.
old-location: fs\fsctl_allow_extended_dasd_io.htm
tech.root: FileIO
ms.assetid: 7d895367-f48f-47db-9ef9-cf20d0ea6782
ms.date: 12/05/2018
ms.keywords: FSCTL_ALLOW_EXTENDED_DASD_IO, FSCTL_ALLOW_EXTENDED_DASD_IO control, FSCTL_ALLOW_EXTENDED_DASD_IO control code [Files], _win32_fsctl_allow_extended_dasd_io, base.fsctl_allow_extended_dasd_io, fs.fsctl_allow_extended_dasd_io, winioctl/FSCTL_ALLOW_EXTENDED_DASD_IO
f1_keywords:
- winioctl/FSCTL_ALLOW_EXTENDED_DASD_IO
dev_langs:
- c++
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
- FSCTL_ALLOW_EXTENDED_DASD_IO
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_ALLOW_EXTENDED_DASD_IO IOCTL

## -description

Signals the file system driver not to perform any I/O boundary checks on partition read or write calls. Instead, boundary checks are performed by the device driver.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_ALLOW_EXTENDED_DASD_IO,     // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  NULL,                             // lpOutBuffer
  0,                                // nOutBufferSize
  (LPDWORD) lpBytesReturned,        // number of bytes returned
  (LPOVERLAPPED) lpOverlapped       // OVERLAPPED structure
);
```

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

A call using the **FSCTL_ALLOW_EXTENDED_DASD_IO** control code should only be used with great caution by programmers familiar with the underlying structure of a hard disk drive and file system. Improper use or inaccurate checking in subsequent write operations to the partition can result in damage to data on the partition, or destruction of the entire partition.

The **FSCTL_ALLOW_EXTENDED_DASD_IO** control code is used to signal the file system driver not to perform any I/O boundary checks on read or write calls made with the specified handle. **FSCTL_ALLOW_EXTENDED_DASD_IO** allows access to hidden sectors, a part of the partition that might exist between the first sector of the partition (the boot parameter block) and the first useful sector of the partition. **FSCTL_ALLOW_EXTENDED_DASD_IO** also allows access to lost clusters, which might exist between the last useful cluster and the end of the partition.

I/O requests issued after this operation are passed directly to the device driver. If these subsequent calls request data beyond the partition boundary, the driver causes them to fail.

For the implications of overlapped I/O on this operation, see the Remarks section of [DeviceIoControl](https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol).

To retrieve a handle to a partition, call [CreateFile](https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea) with the *lpFileName* parameter set to a string of the following form:

\\\\.\\*X*:

where *X* is the drive letter.

The application calling [CreateFile](https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea) must also specify the **FILE_SHARE_READ** and **FILE_SHARE_WRITE** flags in the *dwShareMode* parameter of [CreateFile](https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea). For more information, see the Disk Devices section in [CreateFile](https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea).

To determine the partition structure of the drive and to determine if the system recognizes the partition, use the [IOCTL_DISK_GET_DRIVE_LAYOUT_EX](https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout_ex) or [IOCTL_DISK_GET_DRIVE_LAYOUT](https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout) control code, as appropriate. For similar information on a single partition, use the [IOCTL_DISK_GET_PARTITION_INFO_EX](https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info_ex) or [IOCTL_DISK_GET_PARTITION_INFO](https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info) control code, as appropriate. To determine the size of a cluster, use the [GetDiskFreeSpaceEx](https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespaceexa) or [GetDiskFreeSpace](https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespacea) function, as appropriate.

In Windows Server 2012, this function is supported by the following technologies.

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

[CreateFile](https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-createfilea)

[DeviceIoControl](https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

[File Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/file-management-control-codes)

[GetDiskFreeSpace](https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespacea)

[GetDiskFreeSpaceEx](https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespaceexa)

[IOCTL_DISK_GET_DRIVE_LAYOUT](https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout)

[IOCTL_DISK_GET_DRIVE_LAYOUT_EX](https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout_ex)

[IOCTL_DISK_GET_PARTITION_INFO](https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info)

[IOCTL_DISK_GET_PARTITION_INFO_EX](https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info_ex)

[OVERLAPPED](https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
