---
UID: NI:winioctl.FSCTL_QUERY_USN_JOURNAL
title: FSCTL_QUERY_USN_JOURNAL
description: Queries for information on the current update sequence number (USN) change journal, its records, and its capacity.
helpviewer_keywords: ["FSCTL_QUERY_USN_JOURNAL","FSCTL_QUERY_USN_JOURNAL control","FSCTL_QUERY_USN_JOURNAL control code [Files]","_win32_fsctl_query_usn_journal","base.fsctl_query_usn_journal","fs.fsctl_query_usn_journal","winioctl/FSCTL_QUERY_USN_JOURNAL"]
old-location: fs\fsctl_query_usn_journal.htm
tech.root: FileIO
ms.assetid: 9491b054-934a-4b76-bf77-f397b6386f82
ms.date: 12/05/2018
ms.keywords: FSCTL_QUERY_USN_JOURNAL, FSCTL_QUERY_USN_JOURNAL control, FSCTL_QUERY_USN_JOURNAL control code [Files], _win32_fsctl_query_usn_journal, base.fsctl_query_usn_journal, fs.fsctl_query_usn_journal, winioctl/FSCTL_QUERY_USN_JOURNAL
f1_keywords:
- winioctl/FSCTL_QUERY_USN_JOURNAL
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
- FSCTL_QUERY_USN_JOURNAL
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_QUERY_USN_JOURNAL IOCTL

## -description

Queries for information on the current update sequence number (USN) change journal, its records, and its capacity.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function using the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to volume
  FSCTL_QUERY_USN_JOURNAL,          // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  (LPVOID) lpOutBuffer,             // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
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

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

For more information, see [Creating, Modifying, and Deleting a Change Journal](https://docs.microsoft.com/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal).

To retrieve a handle to a volume, call [CreateFile](../fileapi/nf-fileapi-createfilea.md) with the *lpFileName* parameter set to a string in the following form:

\\\\.\\*X*:

In the preceding string, *X* is the letter identifying the drive on which the volume appears. The volume must be formatted with the NTFS filesystem.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes

An application may experience false positives on CsvFs pause/resume.


## -see-also

* [Change Journals](https://docs.microsoft.com/windows/desktop/FileIO/change-journals)
* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md)
* [GetQueuedCompletionStatus](../ioapiset/nf-ioapiset-getqueuedcompletionstatus.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [USN_JOURNAL_DATA_V0](ns-winioctl-usn_journal_data_v0.md)
* [USN_JOURNAL_DATA_V1](https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh802707(v=vs.85))
* [USN_JOURNAL_DATA_V2](ns-winioctl-usn_journal_data_v2.md)
* [Volume Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes)
