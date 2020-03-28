---
UID: NI:winioctl.FSCTL_LOCK_VOLUME
title: FSCTL_LOCK_VOLUME
description: Locks a volume if it is not in use.
old-location: fs\fsctl_lock_volume.htm
tech.root: FileIO
ms.assetid: b59b5c5e-6719-47a8-8810-14b60204e5ed
ms.date: 12/05/2018
ms.keywords: FSCTL_LOCK_VOLUME, FSCTL_LOCK_VOLUME control, FSCTL_LOCK_VOLUME control code [Files], _win32_fsctl_lock_volume, base.fsctl_lock_volume, fs.fsctl_lock_volume, winioctl/FSCTL_LOCK_VOLUME
f1_keywords:
- winioctl/FSCTL_LOCK_VOLUME
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
- FSCTL_LOCK_VOLUME
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_LOCK_VOLUME IOCTL

## -description

Locks a volume if it is not in use. A locked volume can be accessed only through handles to the file object (*\*hDevice*) that locks the volume. For more information, see the Remarks section.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to a volume
  (DWORD) FSCTL_LOCK_VOLUME,    // dwIoControlCode
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

For more information, see [NTSTATUS Values](https://docs.microsoft.com/windows-hardware/drivers/kernel/ntstatus-values).


## -remarks

The *hDevice* handle passed to [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) must be a handle to a volume, opened for direct access. To retrieve this handle, call [CreateFile](../fileapi/nf-fileapi-createfilea.md) with the *lpFileName* parameter set to a string of the following form: 

\\\\.\\*X*:

where *X* is a hard-drive partition letter, floppy disk drive, or CD-ROM drive. The application must also specify the **FILE_SHARE_READ** and **FILE_SHARE_WRITE** flags in the *dwShareMode* parameter of [CreateFile](../fileapi/nf-fileapi-createfilea.md).

If the specified volume is a system volume or contains a page file, the operation fails.

If there are any open files on the volume, this operation will fail. Conversely, success of this operation indicates there are no open files.

This operation is useful for applications that need exclusive access to a volume for a period of time—for example, disk utility and backup programs.

A locked volume remains locked until one of the following occurs:
* The application uses the [FSCTL_UNLOCK_VOLUME](./ni-winioctl-fsctl_unlock_volume.md) control code to unlock the volume.
* The handle closes, either directly through [CloseHandle](../handleapi/nf-handleapi-closehandle.md), or indirectly when a process terminates.

The system flushes all cached data to the volume before locking it. For example, any data held in a lazy-write cache is written to the volume.

The NTFS file system treats a locked volume as a dismounted volume. The [FSCTL_DISMOUNT_VOLUME](./ni-winioctl-fsctl_dismount_volume.md) control code functions similarly but does not check for open files before dismounting. Note that without a successful lock operation, a dismounted volume may be remounted by any process at any time. This would not be an ideal state for performing a volume backup, for example.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | See comment

On CsvFs Lock Volume, PNP notification will be sent only on the node where the lock request was issued. A lock will succeed only if the CsvFs filter on top of NTFS does not see any opened files.

After acquiring a lock on a CSV volume, you must close the handle used to lock that volume before opening a handle to the volume. Unlocking the volume by using [FSCTL_UNLOCK_VOLUME](./ni-winioctl-fsctl_unlock_volume.md) is not sufficient.


## -see-also

* [CloseHandle](../handleapi/nf-handleapi-closehandle.md)
* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_DISMOUNT_VOLUME](./ni-winioctl-fsctl_dismount_volume.md)
* [FSCTL_UNLOCK_VOLUME](./ni-winioctl-fsctl_unlock_volume.md)
* [Volume Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes)
