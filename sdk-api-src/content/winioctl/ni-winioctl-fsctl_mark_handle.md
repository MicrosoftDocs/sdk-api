---
UID: NI:winioctl.FSCTL_MARK_HANDLE
title: FSCTL_MARK_HANDLE
description: Marks a specified file or directory and its change journal record with information about changes to that file or directory.
helpviewer_keywords: ["FSCTL_MARK_HANDLE","FSCTL_MARK_HANDLE control","FSCTL_MARK_HANDLE control code [Files]","_win32_fsctl_mark_handle","base.fsctl_mark_handle","fs.fsctl_mark_handle","winioctl/FSCTL_MARK_HANDLE"]
old-location: fs\fsctl_mark_handle.htm
tech.root: fs
ms.assetid: c96b49d8-12f3-4281-9f9f-6621769359f0
ms.date: 12/05/2018
ms.keywords: FSCTL_MARK_HANDLE, FSCTL_MARK_HANDLE control, FSCTL_MARK_HANDLE control code [Files], _win32_fsctl_mark_handle, base.fsctl_mark_handle, fs.fsctl_mark_handle, winioctl/FSCTL_MARK_HANDLE
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
 - FSCTL_MARK_HANDLE
 - winioctl/FSCTL_MARK_HANDLE
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
 - FSCTL_MARK_HANDLE
---

# FSCTL_MARK_HANDLE IOCTL


## -description

Marks a specified file or directory and its change journal record with information about changes to that file or directory.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function using the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to file or directory
  FSCTL_MARK_HANDLE,            // dwIoControlCode
  (LPVOID)lpInBuffer,           // input buffer
  (DWORD)nInBufferSize,         // size of input buffer
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

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

**FSCTL_MARK_HANDLE** is the only change journal operation that operates on an individual file or directory. It does not affect anything the user can do with the item. Instead, it adds information to the file or directory, either providing information on how the operating system changed the item or adding a private data stream to the item.

If there are any changes to the file or directory, then the information added with **FSCTL_MARK_HANDLE** is also copied into the USN record created for the file or directory. Note that these two operations can occur independently of each other—for example, it is not necessary for a USN record to exist to be able to mark a file as unable to be defragmented and it is not necessary to mark a file or directory to update the contents of the corresponding USN record. For details on the information with which **FSCTL_MARK_HANDLE** can mark an item (see [MARK_HANDLE_INFO](ns-winioctl-mark_handle_info.md) for more information).

It is not an error to use **FSCTL_MARK_HANDLE** while the volume's change journal is being deleted or is inactive. The appropriate information is applied to the file or directory regardless of the state of the change journal, as long as the change journal exists.

Note that the time stamps may not be updated correctly for a remote file. To ensure consistent results, use unbuffered I/O.

The volume must be NTFS.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

CsvFs always issues **USN_SOURCE_REPLICATION_MANAGEMENT** and **MARK_HANDLE_PROTECT_CLUSTERS** for the files eligible for direct IO.

## -see-also

* [Change Journals](/windows/desktop/FileIO/change-journals)
* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [MARK_HANDLE_INFO](ns-winioctl-mark_handle_info.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)