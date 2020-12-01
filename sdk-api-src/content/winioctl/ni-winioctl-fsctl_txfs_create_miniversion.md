---
UID: NI:winioctl.FSCTL_TXFS_CREATE_MINIVERSION
title: FSCTL_TXFS_CREATE_MINIVERSION
description: Creates a new miniversion for the specified file. Miniversions allow you to refer to a snapshot of the file during a transaction. Miniversions are discarded when a transaction is committed or rolled back.
helpviewer_keywords: ["FSCTL_TXFS_CREATE_MINIVERSION","FSCTL_TXFS_CREATE_MINIVERSION control","FSCTL_TXFS_CREATE_MINIVERSION control code [Files]","fs.fsctl_txfs_create_miniversion","winioctl/FSCTL_TXFS_CREATE_MINIVERSION"]
old-location: fs\fsctl_txfs_create_miniversion.htm
tech.root: fs
ms.assetid: 3d12b149-ab34-46c4-89fc-8ddc12a81fa0
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_CREATE_MINIVERSION, FSCTL_TXFS_CREATE_MINIVERSION control, FSCTL_TXFS_CREATE_MINIVERSION control code [Files], fs.fsctl_txfs_create_miniversion, winioctl/FSCTL_TXFS_CREATE_MINIVERSION
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
 - FSCTL_TXFS_CREATE_MINIVERSION
 - winioctl/FSCTL_TXFS_CREATE_MINIVERSION
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
 - FSCTL_TXFS_CREATE_MINIVERSION
---

# FSCTL_TXFS_CREATE_MINIVERSION IOCTL


## -description

> [!NOTE]
> Microsoft strongly recommends developers utilize alternative means to achieve your application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](/windows/desktop/FileIO/deprecation-of-txf).

Creates a new [miniversion](/windows/win32/fileio/glossary) for the specified file. Miniversions allow you to refer to a snapshot of the file during a transaction.  Miniversions are discarded when a transaction is committed or rolled back.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_TXFS_CREATE_MINIVERSION,    // dwIoControlCode
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

**FSCTL_TXFS_CREATE_MINIVERSION** is a synchronous operation.

If you attempt to create a miniversion in a non-active transaction, **ERROR_INVALID_TRANSACTION** is returned.

**ReFS:**  This code is not supported.

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)