---
UID: NI:winioctl.FSCTL_SET_OBJECT_ID
title: FSCTL_SET_OBJECT_ID
description: Sets the object identifier for the specified file or directory.
helpviewer_keywords: ["FSCTL_SET_OBJECT_ID","FSCTL_SET_OBJECT_ID control","FSCTL_SET_OBJECT_ID control code [Files]","_win32_fsctl_set_object_id","base.fsctl_set_object_id","fs.fsctl_set_object_id","winioctl/FSCTL_SET_OBJECT_ID"]
old-location: fs\fsctl_set_object_id.htm
tech.root: fs
ms.assetid: eb131a33-96c8-40fc-92be-05522676541a
ms.date: 12/05/2018
ms.keywords: FSCTL_SET_OBJECT_ID, FSCTL_SET_OBJECT_ID control, FSCTL_SET_OBJECT_ID control code [Files], _win32_fsctl_set_object_id, base.fsctl_set_object_id, fs.fsctl_set_object_id, winioctl/FSCTL_SET_OBJECT_ID
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
 - FSCTL_SET_OBJECT_ID
 - winioctl/FSCTL_SET_OBJECT_ID
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
 - FSCTL_SET_OBJECT_ID
---

# FSCTL_SET_OBJECT_ID IOCTL


## -description

Sets the object identifier for the specified file or directory.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_SET_OBJECT_ID,              // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
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

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

Object identifiers are used  to track files and directories. They are invisible to most applications and should never be modified by applications. Modifying an object identifier can result in the loss of data from portions of a file, up to and including entire volumes of data. 

Use this operation to explicitly set an object identifier to a value you provide. Attempting to set an object identifier on an object that already has an object identifier will fail. An attempt to use an object identifier that is already in use on the volume will also fail. Use the [FSCTL_CREATE_OR_GET_OBJECT_ID](ni-winioctl-fsctl_create_or_get_object_id.md) operation to have the NTFS file system generate an object identifier if the object does not already have one.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use unbuffered I/O.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | Yes
SMB 3.0 with Scale-out File Shares (SO) | Yes
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | No

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_OBJECTID_BUFFER](ns-winioctl-file_objectid_buffer.md)
* [FSCTL_CREATE_OR_GET_OBJECT_ID](ni-winioctl-fsctl_create_or_get_object_id.md)
* [FSCTL_DELETE_OBJECT_ID](ni-winioctl-fsctl_delete_object_id.md)
* [FSCTL_GET_OBJECT_ID](ni-winioctl-fsctl_get_object_id.md)
* [FSCTL_SET_OBJECT_ID_EXTENDED](ni-winioctl-fsctl_set_object_id_extended.md)
* [Object Identifiers](/windows/desktop/FileIO/distributed-link-tracking-and-object-identifiers)