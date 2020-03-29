---
UID: NI:winioctl.FSCTL_UNLOCK_VOLUME
title: FSCTL_UNLOCK_VOLUME
description: Unlocks a volume.
old-location: fs\fsctl_unlock_volume.htm
tech.root: FileIO
ms.assetid: 84ca7f8d-6a0a-43d6-9970-9c01099eaad4
ms.date: 12/05/2018
ms.keywords: FSCTL_UNLOCK_VOLUME, FSCTL_UNLOCK_VOLUME control, FSCTL_UNLOCK_VOLUME control code [Files], _win32_fsctl_unlock_volume, base.fsctl_unlock_volume, fs.fsctl_unlock_volume, winioctl/FSCTL_UNLOCK_VOLUME
f1_keywords:
- winioctl/FSCTL_UNLOCK_VOLUME
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
- FSCTL_UNLOCK_VOLUME
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_UNLOCK_VOLUME IOCTL

## -description

Unlocks a volume.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to a volume
  FSCTL_UNLOCK_VOLUME,          // dwIoControlCode
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

To lock a volume, use the [FSCTL_LOCK_VOLUME](./ni-winioctl-fsctl_lock_volume.md) control code.

The *hDevice* handle passed to [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) must be a handle to a volume, opened for direct access. To retrieve this handle, call [CreateFile](../fileapi/nf-fileapi-createfilea.md) with the *lpFileName* parameter set to a string of the following form:

\\\\.\\*X*:

where *X* is a hard-drive partition letter, floppy disk drive, or CD-ROM drive. The application must also specify the **FILE_SHARE_READ** and **FILE_SHARE_WRITE** flags in the *dwShareMode* parameter of [CreateFile](../fileapi/nf-fileapi-createfilea.md).

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | See comment

PNP notification is issued only on the node where the FSCTL was issued.

After acquiring a lock on a CSV volume, you must close the handle used to lock that volume before opening a handle to the volume. Unlocking the volume by using **FSCTL_UNLOCK_VOLUME** is not sufficient.


## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_LOCK_VOLUME](./ni-winioctl-fsctl_lock_volume.md)
* [Volume Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes)
