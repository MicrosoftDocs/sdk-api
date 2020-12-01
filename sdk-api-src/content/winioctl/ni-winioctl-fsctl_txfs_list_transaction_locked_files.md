---
UID: NI:winioctl.FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES
title: FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES
description: Returns a list of all files currently locked by the specified transaction. If the return value is ERROR_MORE_DATA, it returns the length of the buffer required to hold the complete list of files at the time of this call.
helpviewer_keywords: ["FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES","FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES control","FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES control code [Files]","fs.fsctl_txfs_list_transaction_locked_files","winioctl/FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES"]
old-location: fs\fsctl_txfs_list_transaction_locked_files.htm
tech.root: fs
ms.assetid: fdef45fd-b197-4428-96c5-ac91b43681b1
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES, FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES control, FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES control code [Files], fs.fsctl_txfs_list_transaction_locked_files, winioctl/FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES
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
 - FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES
 - winioctl/FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES
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
 - FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES
---

# FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES IOCTL


## -description

> [!NOTE]
> Microsoft strongly recommends developers utilize alternative means to achieve your application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](/windows/desktop/FileIO/deprecation-of-txf).

Returns a list of all files currently locked by the specified transaction. If the return value is **ERROR_MORE_DATA**, it returns the length of the buffer required to hold the complete list of files at the time of this call.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                         // handle to device
  FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES, // dwIoControlCode
  (LPVOID) lpInBuffer,                      // input buffer
  (DWORD) nInBufferSize,                    // size of input buffer
  (LPVOID) lpOutBuffer,                     // output buffer
  (DWORD) nOutBufferSize,                   // size of output buffer
  (LPDWORD) lpBytesReturned,                // number of bytes returned
  (LPOVERLAPPED) lpOverlapped );            // OVERLAPPED structure
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

**FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES** is a synchronous operation.

The file path names returned are relative to the volume root.

The number of files returned from one call to the next can change depending on the number of active transactions at any given point in time. If this call returns a request for a larger buffer, that size may or may not be adequate for the next call, based on the number of active transactions at the time of the next call.

**ReFS:**  This code is not supported.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [TXFS_LIST_TRANSACTION_LOCKED_FILES](ns-winioctl-txfs_list_transaction_locked_files.md)
* [TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY](ns-winioctl-txfs_list_transaction_locked_files_entry.md)