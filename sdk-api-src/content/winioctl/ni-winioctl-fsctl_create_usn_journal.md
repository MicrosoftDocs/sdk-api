---
UID: NI:winioctl.FSCTL_CREATE_USN_JOURNAL
title: FSCTL_CREATE_USN_JOURNAL
description: Creates an update sequence number (USN) change journal stream on a target volume, or modifies an existing change journal stream.
helpviewer_keywords: ["FSCTL_CREATE_USN_JOURNAL","FSCTL_CREATE_USN_JOURNAL control","FSCTL_CREATE_USN_JOURNAL control code [Files]","_win32_fsctl_create_usn_journal","base.fsctl_create_usn_journal","fs.fsctl_create_usn_journal","winioctl/FSCTL_CREATE_USN_JOURNAL"]
old-location: fs\fsctl_create_usn_journal.htm
tech.root: FileIO
ms.assetid: 92e737e6-dba6-47f1-a077-e303039e12eb
ms.date: 12/05/2018
ms.keywords: FSCTL_CREATE_USN_JOURNAL, FSCTL_CREATE_USN_JOURNAL control, FSCTL_CREATE_USN_JOURNAL control code [Files], _win32_fsctl_create_usn_journal, base.fsctl_create_usn_journal, fs.fsctl_create_usn_journal, winioctl/FSCTL_CREATE_USN_JOURNAL
f1_keywords:
- winioctl/FSCTL_CREATE_USN_JOURNAL
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
- FSCTL_CREATE_USN_JOURNAL
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_CREATE_USN_JOURNAL IOCTL

## -description

Creates an update sequence number (USN) change journal stream on a target volume, or modifies an existing change journal stream.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to volume
  FSCTL_CREATE_USN_JOURNAL,     // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
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

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

You can use **FSCTL_CREATE_USN_JOURNAL** to create a new change journal stream for a volume. After the creation of the stream, the NTFS file system maintains a change journal for that volume.

You can also use **FSCTL_CREATE_USN_JOURNAL** to modify an existing change journal stream. If a change journal stream already exists, **FSCTL_CREATE_USN_JOURNAL** sets it to the characteristics provided in the [CREATE_USN_JOURNAL_DATA](ns-winioctl-create_usn_journal_data.md) structure. The change journal stream eventually gets larger or is trimmed to the new size limit that [CREATE_USN_JOURNAL_DATA](ns-winioctl-create_usn_journal_data.md) imposes.

For more information, see [Creating, Modifying, and Deleting a Change Journal](https://docs.microsoft.com/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal).

To retrieve a handle to a volume, call [CreateFile](../fileapi/nf-fileapi-createfilea.md) with the *lpFileName* parameter set to a string in the following form:

\\\\.\\*X*:

In the preceding string, *X* is the letter identifying the drive on which the volume appears. The volume must be NTFS 3.0 or later. To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:

**fsutil fsinfo ntfsinfo** *X*<b>:</b>

where *X* is the drive letter of the volume.

In Windows Server 2012, this function is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes


## -see-also

* [CREATE_USN_JOURNAL_DATA](ns-winioctl-create_usn_journal_data.md)
* [Change Journals](https://docs.microsoft.com/windows/desktop/FileIO/change-journals)
* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [Volume Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes)
