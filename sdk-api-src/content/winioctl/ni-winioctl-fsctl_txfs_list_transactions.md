---
UID: NI:winioctl.FSCTL_TXFS_LIST_TRANSACTIONS
title: FSCTL_TXFS_LIST_TRANSACTIONS
description: Returns a list of all the transactions currently involved in the specified resource manager.
helpviewer_keywords: ["FSCTL_TXFS_LIST_TRANSACTIONS","FSCTL_TXFS_LIST_TRANSACTIONS control","FSCTL_TXFS_LIST_TRANSACTIONS control code [Files]","fs.fsctl_txfs_list_transactions","winioctl/FSCTL_TXFS_LIST_TRANSACTIONS"]
old-location: fs\fsctl_txfs_list_transactions.htm
tech.root: fs
ms.assetid: ff319bf0-2bd4-4824-bf97-b9b6eab90915
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_LIST_TRANSACTIONS, FSCTL_TXFS_LIST_TRANSACTIONS control, FSCTL_TXFS_LIST_TRANSACTIONS control code [Files], fs.fsctl_txfs_list_transactions, winioctl/FSCTL_TXFS_LIST_TRANSACTIONS
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
 - FSCTL_TXFS_LIST_TRANSACTIONS
 - winioctl/FSCTL_TXFS_LIST_TRANSACTIONS
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
 - FSCTL_TXFS_LIST_TRANSACTIONS
---

# FSCTL_TXFS_LIST_TRANSACTIONS IOCTL


## -description

> [!NOTE]
> Microsoft strongly recommends developers utilize alternative means to achieve your application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](/windows/desktop/FileIO/deprecation-of-txf).

Returns a list of all the transactions currently involved in the specified resource manager. If the function fails with **ERROR_MORE_DATA**, it returns the length of the buffer required to hold the complete list of transactions at the time of this call.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_TXFS_LIST_TRANSACTIONS,     // dwIoControlCode
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

**FSCTL_TXFS_LIST_TRANSACTIONS** is a synchronous operation.

The number of transactions returned from one call to the next can change depending on the number of active transactions at any given point in time. If this call returns a request for a larger buffer, that size may or may not be adequate for the next call, based on the number of active transactions at the time of the next call. 

**ReFS:**  This code is not supported.

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [TXFS_LIST_TRANSACTIONS](ns-winioctl-txfs_list_transactions.md)
* [TXFS_LIST_TRANSACTIONS_ENTRY](ns-winioctl-txfs_list_transactions_entry.md)