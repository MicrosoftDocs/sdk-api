---
UID: NI:winioctl.FSCTL_DISMOUNT_VOLUME
title: FSCTL_DISMOUNT_VOLUME
description: Dismounts a volume regardless of whether or not the volume is currently in use. For more information, see the Remarks section.
helpviewer_keywords: ["FSCTL_DISMOUNT_VOLUME","FSCTL_DISMOUNT_VOLUME control","FSCTL_DISMOUNT_VOLUME control code [Files]","_win32_fsctl_dismount_volume","base.fsctl_dismount_volume","fs.fsctl_dismount_volume","winioctl/FSCTL_DISMOUNT_VOLUME"]
old-location: fs\fsctl_dismount_volume.htm
tech.root: FileIO
ms.assetid: 8828760c-9635-4c69-9867-c2f5314841e6
ms.date: 12/05/2018
ms.keywords: FSCTL_DISMOUNT_VOLUME, FSCTL_DISMOUNT_VOLUME control, FSCTL_DISMOUNT_VOLUME control code [Files], _win32_fsctl_dismount_volume, base.fsctl_dismount_volume, fs.fsctl_dismount_volume, winioctl/FSCTL_DISMOUNT_VOLUME
f1_keywords:
- winioctl/FSCTL_DISMOUNT_VOLUME
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
- FSCTL_DISMOUNT_VOLUME
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_DISMOUNT_VOLUME IOCTL

## -description

Dismounts a volume regardless of whether or not the volume is currently in use. For more information, see the Remarks section.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to a volume
  (DWORD) FSCTL_DISMOUNT_VOLUME,    // dwIoControlCode
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


### -input-buffer-length


### -output-buffer


### -output-buffer-length


### -in-out-buffer


### -inout-buffer-length


### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).


## -remarks

The **FSCTL_DISMOUNT_VOLUME** control code will attempt to dismount a volume regardless of whether or not any other processes are using the volume, which can have unpredictable results for those processes if they do not hold a lock on the volume. For information about locking a volume, see [FSCTL_LOCK_VOLUME](ni-winioctl-fsctl_lock_volume.md).

The *hDevice* handle passed to [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) must be a handle to a volume, opened for direct access. To retrieve a volume handle, call [CreateFile](../fileapi/nf-fileapi-createfilea.md) with the *lpFileName* parameter set to a string of the following form:

\\\\.\\*X*:

where *X* is a hard-drive partition letter, floppy disk drive, or CD-ROM drive. The application must also specify the **FILE_SHARE_READ** and **FILE_SHARE_WRITE** flags in the *dwShareMode* parameter of [CreateFile](../fileapi/nf-fileapi-createfilea.md).

If the specified volume is a system volume or contains a page file, the operation fails.

If the specified volume is locked by another process, the operation fails. To prevent another process from locking the volume, lock it as soon as you open it.

A dismounted volume has the following properties:
* There are no open files.
* The operating system does detect the volume.

The operating system tries to mount an unmounted volume as soon as an attempt is made to access it. For example, a call to [GetLogicalDrives](../fileapi/nf-fileapi-getlogicaldrives.md) triggers the operating system to mount unmounted volumes.

Dismounting a volume is useful when a volume needs to disappear for a while. For example, an application that changes a volume file system from the FAT file system to the NTFS file system might use the following procedure.

**To change a volume file system**
1. Open a volume.
1. Lock the volume.
1. Format the volume.
1. Dismount the volume.
1. Unlock the volume.
1. Close the volume handle.

A dismounting operation removes the volume from the FAT file system awareness. When the operating system mounts the volume, it appears as an NTFS file system volume.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | See comment

On CsvFs the node where dismount is issued will see a normal dismount sequence. On all other nodes FS will invalidate all the opened files.


## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [ExitThread](../processthreadsapi/nf-processthreadsapi-exitthread.md)
* [FSCTL_LOCK_VOLUME](ni-winioctl-fsctl_lock_volume.md)
* [GetLogicalDrives](../fileapi/nf-fileapi-getlogicaldrives.md)
* [Volume Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes)
