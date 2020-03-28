---
UID: NI:winioctl.FSCTL_ENUM_USN_DATA
title: FSCTL_ENUM_USN_DATA
description: Enumerates the update sequence number (USN) data between two specified boundaries to obtain master file table (MFT) records.
old-location: fs\fsctl_enum_usn_data.htm
tech.root: FileIO
ms.assetid: 44d20401-a2ed-4756-9fda-878a24eab7c3
ms.date: 12/05/2018
ms.keywords: FSCTL_ENUM_USN_DATA, FSCTL_ENUM_USN_DATA control, FSCTL_ENUM_USN_DATA control code [Files], _win32_fsctl_enum_usn_data, base.fsctl_enum_usn_data, fs.fsctl_enum_usn_data, winioctl/FSCTL_ENUM_USN_DATA
f1_keywords:
- winioctl/FSCTL_ENUM_USN_DATA
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
- FSCTL_ENUM_USN_DATA
targetos: Windows
req.typenames: 
req.redist: 
---

# FSCTL_ENUM_USN_DATA IOCTL

## -description

Enumerates  the update sequence number (USN) data between two specified boundaries to obtain master file table (MFT) records.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to volume
  FSCTL_ENUM_USN_DATA,          // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
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

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../api/ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

To enumerate files on a volume, use the **FSCTL_ENUM_USN_DATA** operation one or more times. On the first call, set the starting point, the **StartFileReferenceNumber** member of the [MFT_ENUM_DATA](./ns-winioctl-mft_enum_data_v0.md) structure, to `(DWORDLONG)0`. Each call to **FSCTL_ENUM_USN_DATA** retrieves the starting point for the subsequent call as the first entry in the output buffer.

By comparing To identify recent changes to a volume, use the [FSCTL_READ_USN_JOURNAL](./ni-winioctl-fsctl_read_usn_journal.md) control code.

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

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_READ_USN_JOURNAL](./ni-winioctl-fsctl_read_usn_journal.md)
* [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md)
* [MFT_ENUM_DATA](./ns-winioctl-mft_enum_data_v0.md)
* [OVERLAPPED](..minwinbase/ns-minwinbase-overlapped.md)
* [USN_RECORD](./ns-winioctl-usn_record_v2.md)
* [Volume Management Control Codes](https://docs.microsoft.com/windows/desktop/FileIO/volume-management-control-codes)
