---
UID: NI:winioctl.FSCTL_GET_OBJECT_ID
title: FSCTL_GET_OBJECT_ID
description: Retrieves the object identifier for the specified file or directory.
helpviewer_keywords: ["FSCTL_GET_OBJECT_ID","FSCTL_GET_OBJECT_ID control","FSCTL_GET_OBJECT_ID control code [Files]","_win32_fsctl_get_object_id","base.fsctl_get_object_id","fs.fsctl_get_object_id","winioctl/FSCTL_GET_OBJECT_ID"]
old-location: fs\fsctl_get_object_id.htm
tech.root: fs
ms.assetid: 60eb4218-424e-4101-a012-3fde66f4f4fe
ms.date: 12/05/2018
ms.keywords: FSCTL_GET_OBJECT_ID, FSCTL_GET_OBJECT_ID control, FSCTL_GET_OBJECT_ID control code [Files], _win32_fsctl_get_object_id, base.fsctl_get_object_id, fs.fsctl_get_object_id, winioctl/FSCTL_GET_OBJECT_ID
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
 - FSCTL_GET_OBJECT_ID
 - winioctl/FSCTL_GET_OBJECT_ID
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
 - FSCTL_GET_OBJECT_ID
---

# FSCTL_GET_OBJECT_ID IOCTL


## -description

Retrieves the object identifier for the specified file or directory.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to file object
  FSCTL_GET_OBJECT_ID,        // dwIoControlCode
  NULL,                       // lpInBuffer
  0,                          // nInBufferSize
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```

## -ioctlparameters

### -param hDevice [in]

A handle to the file object.

To retrieve a device handle, call the [**CreateFile**](../fileapi/nf-fileapi-createfilew.md) function.

### -param dwIoControlCode [in]

The control code for the operation.

Use **FSCTL_GET_OBJECT_ID** for this operation.

### -param lpInBuffer [in, optional]

Not used with this operation. Set to **NULL**.

### -param nInBufferSize [in]

The size of the input buffer, in bytes. Set to 0 (zero).

### -param lpOutBuffer [out, optional]

A pointer to the output buffer that is to receive the [**FILE_OBJECTID_BUFFER**](ns-winioctl-file_objectid_buffer.md) data returned by the operation.

### -param nOutBufferSize [in]

The size of the output buffer, in bytes. It must be >= **sizeof**(FILE_OBJECTID_BUFFER).

### -param lpBytesReturned [out, optional]

A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.

### -param lpOverlapped [in, out, optional]

A pointer to an [**OVERLAPPED**](../minwinbase/ns-minwinbase-overlapped.md) structure.

### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

Object identifiers are used to track files and directories. They are invisible to most applications and should never be modified by applications. Modifying an object identifier can result in the loss of data from portions of a file, up to and including entire volumes of data.

If there is no object identifier associated with the specified handle, none is created and an error is returned. To retrieve an existing object identifier or generate one if there is no existing object identifier in one step, use [FSCTL_CREATE_OR_GET_OBJECT_ID](ni-winioctl-fsctl_create_or_get_object_id.md). To manually assign an object identifier, use [FSCTL_SET_OBJECT_ID](ni-winioctl-fsctl_set_object_id.md). 

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
* [FSCTL_SET_OBJECT_ID](ni-winioctl-fsctl_set_object_id.md)
* [FSCTL_SET_OBJECT_ID_EXTENDED](ni-winioctl-fsctl_set_object_id_extended.md)
* [Object Identifiers](/windows/desktop/FileIO/distributed-link-tracking-and-object-identifiers)
