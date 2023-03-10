---
UID: NI:winioctl.FSCTL_OPLOCK_BREAK_ACK_NO_2
title: FSCTL_OPLOCK_BREAK_ACK_NO_2
description: Responds to notification that an opportunistic lock on a file is about to be broken. Use this operation to unlock all opportunistic locks on the file but keep the file open.
helpviewer_keywords: ["FSCTL_OPLOCK_BREAK_ACK_NO_2","FSCTL_OPLOCK_BREAK_ACK_NO_2 control","FSCTL_OPLOCK_BREAK_ACK_NO_2 control code [Files]","_win32_fsctl_oplock_break_ack_no_2","base.fsctl_oplock_break_ack_no_2","fs.fsctl_oplock_break_ack_no_2","winioctl/FSCTL_OPLOCK_BREAK_ACK_NO_2"]
old-location: fs\fsctl_oplock_break_ack_no_2.htm
tech.root: fs
ms.assetid: 1624fa94-fcf4-4804-b659-84de5ccc77dc
ms.date: 12/05/2018
ms.keywords: FSCTL_OPLOCK_BREAK_ACK_NO_2, FSCTL_OPLOCK_BREAK_ACK_NO_2 control, FSCTL_OPLOCK_BREAK_ACK_NO_2 control code [Files], _win32_fsctl_oplock_break_ack_no_2, base.fsctl_oplock_break_ack_no_2, fs.fsctl_oplock_break_ack_no_2, winioctl/FSCTL_OPLOCK_BREAK_ACK_NO_2
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
 - FSCTL_OPLOCK_BREAK_ACK_NO_2
 - winioctl/FSCTL_OPLOCK_BREAK_ACK_NO_2
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
 - FSCTL_OPLOCK_BREAK_ACK_NO_2
---

# FSCTL_OPLOCK_BREAK_ACK_NO_2 IOCTL


## -description

Responds to notification that an opportunistic lock on a file is about to be broken. Use this operation to unlock all opportunistic locks on the file but keep the file open.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function using the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to file
  FSCTL_OPLOCK_BREAK_ACK_NO_2,      // dwIoControlCode
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

This operation is used only by client applications that have requested an opportunistic lock from a local server. Client applications requesting opportunistic locks from remote servers must not request them directly—the network redirector transparently requests opportunistic locks for the application.

For the implications of overlapped I/O on this operation, see the Remarks section of the [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) topic.

When you receive notification that an opportunistic lock on a file is about to be broken, use the **FSCTL_OPLOCK_BREAK_ACK_NO_2** control code to indicate to the server that you want to relinquish any opportunistic locks but plan to keep the file open. If the operation returns the error code **ERROR_IO_PENDING**, the server has granted a level 2 lock on the file.

One alternative to using **FSCTL_OPLOCK_BREAK_ACK_NO_2** is to indicate that the application is about to close the file anyway. Use the [FSCTL_OPBATCH_ACK_CLOSE_PENDING](ni-winioctl-fsctl_opbatch_ack_close_pending.md) control code for this response.

Another alternative, used if the lock being broken is an exclusive opportunistic lock, is to indicate the file should receive a level 2 opportunistic lock instead. Use the [FSCTL_OPLOCK_BREAK_ACKNOWLEDGE](ni-winioctl-fsctl_oplock_break_acknowledge.md) control code for this response.

Applications are notified that an opportunistic lock is broken by using the **hEvent** member of the [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md) structure associated with the file on which the opportunistic lock is broken. Applications may also use functions such as [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md) and [HasOverlappedIoCompleted](../winbase/nf-winbase-hasoverlappediocompleted.md).

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
* [FSCTL_OPBATCH_ACK_CLOSE_PENDING](ni-winioctl-fsctl_opbatch_ack_close_pending.md)
* [FSCTL_OPLOCK_BREAK_ACKNOWLEDGE](ni-winioctl-fsctl_oplock_break_acknowledge.md)
* [GetOverlappedResult](../ioapiset/nf-ioapiset-getoverlappedresult.md)
* [HasOverlappedIoCompleted](../winbase/nf-winbase-hasoverlappediocompleted.md)
* [OVERLAPPED](../minwinbase/ns-minwinbase-overlapped.md)
* [Oplock Semantics](/windows-hardware/drivers/ifs/oplock-semantics)
* [Opportunistic Locks](/windows/desktop/FileIO/opportunistic-locks)