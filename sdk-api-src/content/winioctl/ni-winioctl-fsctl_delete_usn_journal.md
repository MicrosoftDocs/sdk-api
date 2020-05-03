---
UID: NI:winioctl.FSCTL_DELETE_USN_JOURNAL
title: FSCTL_DELETE_USN_JOURNAL
description: Deletes the update sequence number (USN) change journal on a volume, or waits for notification of change journal deletion.
helpviewer_keywords: ["FSCTL_DELETE_USN_JOURNAL","FSCTL_DELETE_USN_JOURNAL control","FSCTL_DELETE_USN_JOURNAL control code [Files]","_win32_fsctl_delete_usn_journal","base.fsctl_delete_usn_journal","fs.fsctl_delete_usn_journal","winioctl/FSCTL_DELETE_USN_JOURNAL"]
old-location: fs\fsctl_delete_usn_journal.htm
tech.root: FileIO
ms.assetid: 6c85464d-019b-4923-9acf-152b4ee8c31b
ms.date: 12/05/2018
ms.keywords: FSCTL_DELETE_USN_JOURNAL, FSCTL_DELETE_USN_JOURNAL control, FSCTL_DELETE_USN_JOURNAL control code [Files], _win32_fsctl_delete_usn_journal, base.fsctl_delete_usn_journal, fs.fsctl_delete_usn_journal, winioctl/FSCTL_DELETE_USN_JOURNAL
f1_keywords:
- winioctl/FSCTL_DELETE_USN_JOURNAL
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
- FSCTL_DELETE_USN_JOURNAL
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_DELETE_USN_JOURNAL IOCTL

## -description

Deletes the update sequence number (USN) change journal on a volume, or waits for notification of change journal deletion.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to volume
  FSCTL_DELETE_USN_JOURNAL,     // dwIoControlCode
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

You can use **FSCTL_DELETE_USN_JOURNAL** to delete a change journal. The NTFS file system starts a deletion operation and returns immediately to the calling process, unless the **USN_DELETE_FLAG_NOTIFY** flag is set in the **DeleteFlags** member of [DELETE_USN_JOURNAL_DATA](ns-winioctl-delete_usn_journal_data.md).

If the **USN_DELETE_FLAG_NOTIFY** and **USN_DELETE_FLAG_DELETE** flags are both set, a call to **FSCTL_DELETE_USN_JOURNAL** begins the deletion process. Then the call either blocks the calling thread and waits for the deletion (on a synchronous or non-overlapped call), or sets up event notification by using an I/O completion port or other mechanism, and returns (on an asynchronous or overlapped call).

You can also use **FSCTL_DELETE_USN_JOURNAL** to receive notification that a change journal deletion is complete, by setting only **USN_DELETE_FLAG_NOTIFY**. If you do so, the **FSCTL_DELETE_USN_JOURNAL** operation either waits until the deletion completes before returning (on a synchronous or non-overlapped call), or sets up event notification by using an I/O completion port or other mechanism (on an asynchronous or overlapped call).

The deletion on which an application receives notification may have been initiated by the current process, or some other process. For example, when an application is started, it can use **FSCTL_DELETE_USN_JOURNAL** to determine if a deletion started by some other process is in progress and if it is, exit.

Complete deletion of a change journal requires a scan of the volume where the change journal resides, which may take a long time on a volume with many files. The operation continues to completion even across system restarts. Attempts to create, modify, delete, or query the change journal while deletion is in progress fail and return the error code **ERROR_JOURNAL_DELETE_IN_PROGRESS**.

The **FSCTL_DELETE_USN_JOURNAL** operation has a significant performance cost, so it should be used sparingly. An administrator should delete a journal when the current USN value approaches that of the maximum possible USN value.

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
Cluster Shared Volume File System (CsvFS) | Yes


## -see-also

* [CREATE_USN_JOURNAL_DATA](ns-winioctl-create_usn_journal_data.md)
* [Change Journals](https://docs.microsoft.com/windows/desktop/FileIO/change-journals)
* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DELETE_USN_JOURNAL_DATA](ns-winioctl-delete_usn_journal_data.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_CREATE_USN_JOURNAL](ni-winioctl-fsctl_create_usn_journal.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [Volume Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes)
