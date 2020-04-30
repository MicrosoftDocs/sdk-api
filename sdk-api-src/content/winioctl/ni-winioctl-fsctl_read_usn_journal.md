---
UID: NI:winioctl.FSCTL_READ_USN_JOURNAL
title: FSCTL_READ_USN_JOURNAL
description: Retrieves the set of update sequence number (USN) change journal records between two specified USN values.
helpviewer_keywords: ["FSCTL_READ_USN_JOURNAL","FSCTL_READ_USN_JOURNAL control","FSCTL_READ_USN_JOURNAL control code [Files]","_win32_fsctl_read_usn_journal","base.fsctl_read_usn_journal","fs.fsctl_read_usn_journal","winioctl/FSCTL_READ_USN_JOURNAL"]
old-location: fs\fsctl_read_usn_journal.htm
tech.root: FileIO
ms.assetid: 205de464-7e96-477b-9115-e819719b160e
ms.date: 12/05/2018
ms.keywords: FSCTL_READ_USN_JOURNAL, FSCTL_READ_USN_JOURNAL control, FSCTL_READ_USN_JOURNAL control code [Files], _win32_fsctl_read_usn_journal, base.fsctl_read_usn_journal, fs.fsctl_read_usn_journal, winioctl/FSCTL_READ_USN_JOURNAL
f1_keywords:
- winioctl/FSCTL_READ_USN_JOURNAL
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
- FSCTL_READ_USN_JOURNAL
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_READ_USN_JOURNAL IOCTL

## -description

Retrieves  the set of update sequence number (USN) change journal records between two specified USN values.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to volume
  FSCTL_READ_USN_JOURNAL,           // dwIoControlCode
  (LPVOID) lpInBuffer,              // input buffer
  (DWORD) nInBufferSize,            // size of input buffer
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

There are two [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) control codes that return USN records, **FSCTL_READ_USN_JOURNAL** and [FSCTL_ENUM_USN_DATA](ni-winioctl-fsctl_enum_usn_data.md). Use the latter when you want a listing (enumeration) of the USN records between two USNs. Use the former when you want to select by USN.

For more information, see [Creating, Modifying, and Deleting a Change Journal](https://docs.microsoft.com/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal).

To retrieve a handle to a volume, call [CreateFile](../fileapi/nf-fileapi-createfilea.md) with the *lpFileName* parameter set to a string in the following form:

\\\\.\\*X*:

In the preceding string, *X* is the letter identifying the drive on which the volume appears. The volume must be NTFS.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | See comment

An application may experience false positives on CsvFs pause/resume.


#### Examples

For an example, see [Walking a Buffer of Change Journal Records](https://docs.microsoft.com/windows/desktop/FileIO/walking-a-buffer-of-change-journal-records).


## -see-also

* [Change Journals](https://docs.microsoft.com/windows/desktop/FileIO/change-journals)
* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_ENUM_USN_DATA](ni-winioctl-fsctl_enum_usn_data.md)
* [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md)
* [GetQueuedCompletionStatus](../ioapiset/nf-ioapiset-getqueuedcompletionstatus.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [READ_USN_JOURNAL_DATA](ns-winioctl-read_usn_journal_data_v0.md)
* [USN_RECORD](ns-winioctl-usn_record_v2.md)
* [Volume Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes)
