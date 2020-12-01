---
UID: NI:winioctl.FSCTL_TXFS_TRANSACTION_ACTIVE
title: FSCTL_TXFS_TRANSACTION_ACTIVE
description: Returns a Boolean value that indicates if there were any transactions active on the associated volume when the snapshot was taken. This call is only valid for read-only snapshot volumes.
helpviewer_keywords: ["FSCTL_TXFS_TRANSACTION_ACTIVE","FSCTL_TXFS_TRANSACTION_ACTIVE control","FSCTL_TXFS_TRANSACTION_ACTIVE control code [Files]","fs.fsctl_txfs_transaction_active","winioctl/FSCTL_TXFS_TRANSACTION_ACTIVE"]
old-location: fs\fsctl_txfs_transaction_active.htm
tech.root: fs
ms.assetid: c55802b7-9c56-48ee-9d0b-777f06fbeff1
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_TRANSACTION_ACTIVE, FSCTL_TXFS_TRANSACTION_ACTIVE control, FSCTL_TXFS_TRANSACTION_ACTIVE control code [Files], fs.fsctl_txfs_transaction_active, winioctl/FSCTL_TXFS_TRANSACTION_ACTIVE
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FSCTL_TXFS_TRANSACTION_ACTIVE
 - winioctl/FSCTL_TXFS_TRANSACTION_ACTIVE
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
 - FSCTL_TXFS_TRANSACTION_ACTIVE
---

# FSCTL_TXFS_TRANSACTION_ACTIVE IOCTL


## -description

> [!NOTE]
> Microsoft strongly recommends developers utilize alternative means to achieve your application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](/windows/desktop/FileIO/deprecation-of-txf).

Returns a Boolean value that  indicates if there were any transactions  active on the associated volume when the snapshot was taken.  This call is only valid for read-only snapshot volumes.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_TXFS_TRANSACTION_ACTIVE,    // dwIoControlCode
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

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

**FSCTL_TXFS_TRANSACTION_ACTIVE** is a synchronous operation.

If the **TransactionsActiveAtSnapshot** member of the [TXFS_TRANSACTION_ACTIVE_INFO](ns-winioctl-txfs_transaction_active_info.md) structure is **TRUE**, you must remount the snapshot read/write, and run your recovery operations.

**ReFS:**  This code is not supported.

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [TXFS_TRANSACTION_ACTIVE_INFO](ns-winioctl-txfs_transaction_active_info.md)