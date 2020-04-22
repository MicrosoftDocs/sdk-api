---
UID: NI:winioctl.FSCTL_READ_FILE_USN_DATA
title: FSCTL_READ_FILE_USN_DATA
description: Retrieves the update sequence number (USN) change-journal information for the specified file or directory.
helpviewer_keywords: ["FSCTL_READ_FILE_USN_DATA","FSCTL_READ_FILE_USN_DATA control","FSCTL_READ_FILE_USN_DATA control code [Files]","base.fsctl_read_file_usn_data","fs.fsctl_read_file_usn_data","winioctl/FSCTL_READ_FILE_USN_DATA"]
old-location: fs\fsctl_read_file_usn_data.htm
tech.root: FileIO
ms.assetid: 22c797c8-87c8-4d45-b163-4573e6ed17e1
ms.date: 12/05/2018
ms.keywords: FSCTL_READ_FILE_USN_DATA, FSCTL_READ_FILE_USN_DATA control, FSCTL_READ_FILE_USN_DATA control code [Files], base.fsctl_read_file_usn_data, fs.fsctl_read_file_usn_data, winioctl/FSCTL_READ_FILE_USN_DATA
f1_keywords:
- winioctl/FSCTL_READ_FILE_USN_DATA
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
- FSCTL_READ_FILE_USN_DATA
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_READ_FILE_USN_DATA IOCTL

## -description

Retrieves the update sequence number (USN) change-journal information for the specified file or directory.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_READ_FILE_USN_DATA,         // dwIoControlCode
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

If the call succeeds, the  members of the returned [USN_RECORD_V2](ns-winioctl-usn_record_v2.md) or [USN_RECORD_V3](ns-winioctl-usn_record_v3.md) structure are valid except for the following members: **TimeStamp**, **Reason**, and **SourceInfo**. The **Usn** member represents the last USN written to the journal for this file or directory.

For more information, see [Creating, Modifying, and Deleting a Change Journal](https://docs.microsoft.com/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal).

To retrieve a handle to a volume, call [CreateFile](../fileapi/nf-fileapi-createfilea.md) with the *lpFileName* parameter set to a string in the following form:

\\\\.\\*X*:

In the preceding string, *X* is the letter identifying the drive on which the volume appears. The volume must be ReFS or NTFS 3.0 or later. To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:

**FSUtil.exe FSInfo NTFSInfo** _X_**:**

where *X* is the drive letter of the volume.

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes


## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [USN_RECORD](ns-winioctl-usn_record_v2.md)
* [Volume Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes)
