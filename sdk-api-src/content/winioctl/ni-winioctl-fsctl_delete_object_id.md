---
UID: NI:winioctl.FSCTL_DELETE_OBJECT_ID
title: FSCTL_DELETE_OBJECT_ID
description: Removes the object identifier from a specified file or directory.
helpviewer_keywords: ["FSCTL_DELETE_OBJECT_ID","FSCTL_DELETE_OBJECT_ID control","FSCTL_DELETE_OBJECT_ID control code [Files]","_win32_fsctl_delete_object_id","base.fsctl_delete_object_id","fs.fsctl_delete_object_id","winioctl/FSCTL_DELETE_OBJECT_ID"]
old-location: fs\fsctl_delete_object_id.htm
tech.root: FileIO
ms.assetid: 6698ca1d-d603-4f8d-9737-6dcb9be24e3a
ms.date: 12/05/2018
ms.keywords: FSCTL_DELETE_OBJECT_ID, FSCTL_DELETE_OBJECT_ID control, FSCTL_DELETE_OBJECT_ID control code [Files], _win32_fsctl_delete_object_id, base.fsctl_delete_object_id, fs.fsctl_delete_object_id, winioctl/FSCTL_DELETE_OBJECT_ID
f1_keywords:
- winioctl/FSCTL_DELETE_OBJECT_ID
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
- FSCTL_DELETE_OBJECT_ID
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_DELETE_OBJECT_ID IOCTL

## -description

Removes the object identifier from a specified file or directory. The underlying object is not deleted.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_DELETE_OBJECT_ID,       // dwIoControlCode
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

Object identifiers are used  to track  files and directories. They are invisible to most applications and should never be modified by applications. Modifying an object identifier can result in the loss of data from portions of a file, up to and including entire volumes of data.

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
* [FSCTL_CREATE_OR_GET_OBJECT_ID](ni-winioctl-fsctl_create_or_get_object_id.md)
* [FSCTL_GET_OBJECT_ID](ni-winioctl-fsctl_get_object_id.md)
* [FSCTL_SET_OBJECT_ID](ni-winioctl-fsctl_set_object_id.md)
* [FSCTL_SET_OBJECT_ID_EXTENDED](ni-winioctl-fsctl_set_object_id_extended.md)
* [Object Identifiers](https://docs.microsoft.com/windows/desktop/FileIO/distributed-link-tracking-and-object-identifiers)
