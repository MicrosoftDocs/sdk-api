---
UID: NI:winioctl.FSCTL_WRITE_USN_CLOSE_RECORD
title: FSCTL_WRITE_USN_CLOSE_RECORD
description: Generates a record in the update sequence number (USN) change journal stream for the input file.
helpviewer_keywords: ["FSCTL_WRITE_USN_CLOSE_RECORD","FSCTL_WRITE_USN_CLOSE_RECORD control","FSCTL_WRITE_USN_CLOSE_RECORD control code [Files]","_win32_fsctl_write_usn_close_record","base.fsctl_write_usn_close_record","fs.fsctl_write_usn_close_record","winioctl/FSCTL_WRITE_USN_CLOSE_RECORD"]
old-location: fs\fsctl_write_usn_close_record.htm
tech.root: FileIO
ms.assetid: d7e0ad05-8ad5-4672-bd32-5a3b1dd0a6ea
ms.date: 12/05/2018
ms.keywords: FSCTL_WRITE_USN_CLOSE_RECORD, FSCTL_WRITE_USN_CLOSE_RECORD control, FSCTL_WRITE_USN_CLOSE_RECORD control code [Files], _win32_fsctl_write_usn_close_record, base.fsctl_write_usn_close_record, fs.fsctl_write_usn_close_record, winioctl/FSCTL_WRITE_USN_CLOSE_RECORD
f1_keywords:
- winioctl/FSCTL_WRITE_USN_CLOSE_RECORD
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
- FSCTL_WRITE_USN_CLOSE_RECORD
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_WRITE_USN_CLOSE_RECORD IOCTL

## -description

Generates a record in the update sequence number (USN) change journal stream for the input file. This record will have the **USN_REASON_CLOSE** flag.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to volume
  FSCTL_WRITE_USN_CLOSE_RECORD,     // dwIoControlCode
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

For the implications of overlapped I/O on this operation, see the Remarks section for [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md).

You can use **FSCTL_WRITE_USN_CLOSE_RECORD** to force a close record into the change journal for the input handle. The close record will contain any current USN reasons for this file as well. The output buffer will return the USN value associated with this operation.

For more information, see [Creating, Modifying, and Deleting a Change Journal](https://docs.microsoft.com/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal).

To retrieve a handle to a volume, call [CreateFile](../fileapi/nf-fileapi-createfilea.md) with the *lpFileName* parameter set to a string in the following form:

\\\\.\\*X*:

In the preceding string, *X* is the letter identifying the drive on which the volume appears. The volume must be NTFS 3.0 or later. To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:

**fsutil fsinfo ntfsinfo** _X_**:**

where *X* is the drive letter of the volume.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes


<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If <b>FSCTL_WRITE_USN_CLOSE_RECORD</b> is called 
      with a handle that is locked by a transaction, it always fails.


## -see-also

* [Change Journals](https://docs.microsoft.com/windows/desktop/FileIO/change-journals)
* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [Volume Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes)
