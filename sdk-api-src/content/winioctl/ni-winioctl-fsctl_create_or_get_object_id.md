---
UID: NI:winioctl.FSCTL_CREATE_OR_GET_OBJECT_ID
title: FSCTL_CREATE_OR_GET_OBJECT_ID
description: Retrieves the object identifier for the specified file or directory. If no object identifier exists, using FSCTL_CREATE_OR_GET_OBJECT_ID creates one.
helpviewer_keywords: ["FSCTL_CREATE_OR_GET_OBJECT_ID","FSCTL_CREATE_OR_GET_OBJECT_ID control","FSCTL_CREATE_OR_GET_OBJECT_ID control code [Files]","_win32_fsctl_create_or_get_object_id","base.fsctl_create_or_get_object_id","fs.fsctl_create_or_get_object_id","winioctl/FSCTL_CREATE_OR_GET_OBJECT_ID"]
old-location: fs\fsctl_create_or_get_object_id.htm
tech.root: fs
ms.assetid: 78a2dfa0-a095-4ca3-bfbb-4535086dee4a
ms.date: 12/05/2018
ms.keywords: FSCTL_CREATE_OR_GET_OBJECT_ID, FSCTL_CREATE_OR_GET_OBJECT_ID control, FSCTL_CREATE_OR_GET_OBJECT_ID control code [Files], _win32_fsctl_create_or_get_object_id, base.fsctl_create_or_get_object_id, fs.fsctl_create_or_get_object_id, winioctl/FSCTL_CREATE_OR_GET_OBJECT_ID
f1_keywords:
- winioctl/FSCTL_CREATE_OR_GET_OBJECT_ID
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
- FSCTL_CREATE_OR_GET_OBJECT_ID
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_CREATE_OR_GET_OBJECT_ID IOCTL

## -description

Retrieves the object identifier for the specified file or directory. If no object identifier exists, using **FSCTL_CREATE_OR_GET_OBJECT_ID** creates one.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,              // handle to device
  FSCTL_CREATE_OR_GET_OBJECT_ID, // dwIoControlCode
  NULL,                          // lpInBuffer
  0,                             // nInBufferSize
  (LPVOID) lpOutBuffer,          // output buffer
  (DWORD) nOutBufferSize,        // size of output buffer
  (LPDWORD) lpBytesReturned,     // number of bytes returned
  (LPOVERLAPPED) lpOverlapped    // OVERLAPPED structure
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

Object identifiers are used to track  files and directories. They are invisible to most applications and should never be modified by applications. Modifying an object identifier can result in the loss of data from portions of a file, up to and including entire volumes of data.

This operation creates an object identifier if the object does not already have one. To test for the presence of an object identifier, and retrieve it if it exists, use the [FSCTL_GET_OBJECT_ID](ni-winioctl-fsctl_get_object_id.md) operation. To create an object identifier without first testing for the presence of one, use the [FSCTL_SET_OBJECT_ID](ni-winioctl-fsctl_set_object_id.md) operation.

In Windows Server 2012, this function is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | Yes
SMB 3.0 Transparent Failover (TFO) | Yes
SMB 3.0 with Scale-out File Shares (SO) | Yes
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | No


## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_OBJECTID_BUFFER](ns-winioctl-file_objectid_buffer.md)
* [FSCTL_DELETE_OBJECT_ID](ni-winioctl-fsctl_delete_object_id.md)
* [FSCTL_GET_OBJECT_ID](ni-winioctl-fsctl_get_object_id.md)
* [FSCTL_SET_OBJECT_ID](ni-winioctl-fsctl_set_object_id.md)
* [FSCTL_SET_OBJECT_ID_EXTENDED](ni-winioctl-fsctl_set_object_id_extended.md)
* [Object Identifiers](https://docs.microsoft.com/windows/desktop/FileIO/distributed-link-tracking-and-object-identifiers)
