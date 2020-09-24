---
UID: NI:winioctl.FSCTL_OPBATCH_ACK_CLOSE_PENDING
title: FSCTL_OPBATCH_ACK_CLOSE_PENDING
description: Notifies a server that a client application is ready to close a file.
helpviewer_keywords: ["FSCTL_OPBATCH_ACK_CLOSE_PENDING","FSCTL_OPBATCH_ACK_CLOSE_PENDING control","FSCTL_OPBATCH_ACK_CLOSE_PENDING control code [Files]","_win32_fsctl_opbatch_ack_close_pending","base.fsctl_opbatch_ack_close_pending","fs.fsctl_opbatch_ack_close_pending","winioctl/FSCTL_OPBATCH_ACK_CLOSE_PENDING"]
old-location: fs\fsctl_opbatch_ack_close_pending.htm
tech.root: fs
ms.assetid: 09014adb-e65e-4e9c-9f29-4bdbe61ea695
ms.date: 12/05/2018
ms.keywords: FSCTL_OPBATCH_ACK_CLOSE_PENDING, FSCTL_OPBATCH_ACK_CLOSE_PENDING control, FSCTL_OPBATCH_ACK_CLOSE_PENDING control code [Files], _win32_fsctl_opbatch_ack_close_pending, base.fsctl_opbatch_ack_close_pending, fs.fsctl_opbatch_ack_close_pending, winioctl/FSCTL_OPBATCH_ACK_CLOSE_PENDING
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
 - FSCTL_OPBATCH_ACK_CLOSE_PENDING
 - winioctl/FSCTL_OPBATCH_ACK_CLOSE_PENDING
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
 - FSCTL_OPBATCH_ACK_CLOSE_PENDING
---

# FSCTL_OPBATCH_ACK_CLOSE_PENDING IOCTL


## -description

Notifies a server that a client application is ready to close a file. Use this operation after notification that an opportunistic lock on a file is ready to be broken. 

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function by using the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to file
  FSCTL_OPBATCH_ACK_CLOSE_PENDING,  // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  NULL,                             // lpOutBuffer
  0,                                // nOutBufferSize
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

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

Before you call this function do not make assumptions about the number of available virtual channels, because the system and other plug-ins might have reserved virtual channels. Always check for a **CHANNEL_RC_TOO_MANY_CHANNELS** return code after calling this function.

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

Use the **FSCTL_OPBATCH_ACK_CLOSE_PENDING** control code when you are notified that an opportunistic lock on a file is ready to be broken, and you intend to close the file soon. This operation does not request a new opportunistic lock.

If you do not intend to close a file, you can use the [FSCTL_OPLOCK_BREAK_ACKNOWLEDGE](ni-winioctl-fsctl_oplock_break_acknowledge.md) or [FSCTL_OPLOCK_BREAK_ACK_NO_2](ni-winioctl-fsctl_oplock_break_ack_no_2.md) control code to respond to the notification. The former, used if the lock being broken is an exclusive opportunistic lock, indicates the file should receive a level 2 opportunistic lock instead. The latter requests the file be kept open but loses all locking.

Applications are notified that an opportunistic lock is broken by using the **hEvent** member of the [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md) structure that is associated with a file on which an opportunistic lock is broken. Applications can also use functions such as [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md) and [HasOverlappedIoCompleted](../winbase/nf-winbase-hasoverlappediocompleted.md).

In Windows 8 and Windows Server 2012, this code is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol | No
SMB 3.0 Transparent Failover (TFO) | No
SMB 3.0 with Scale-out File Shares (SO) | No
Cluster Shared Volume File System (CsvFS) | Yes
Resilient File System (ReFS) | Yes

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_OPLOCK_BREAK_ACKNOWLEDGE](ni-winioctl-fsctl_oplock_break_acknowledge.md)
* [FSCTL_OPLOCK_BREAK_ACK_NO_2](ni-winioctl-fsctl_oplock_break_ack_no_2.md)
* [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md)
* [HasOverlappedIoCompleted](../winbase/nf-winbase-hasoverlappediocompleted.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [Opportunistic Locks](/windows/desktop/FileIO/opportunistic-locks)