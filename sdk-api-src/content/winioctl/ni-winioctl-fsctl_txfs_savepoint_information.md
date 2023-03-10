---
UID: NI:winioctl.FSCTL_TXFS_SAVEPOINT_INFORMATION
title: FSCTL_TXFS_SAVEPOINT_INFORMATION
description: The FSCTL_TXFS_SAVEPOINT_INFORMATION control code controls setting, clearing, and rolling back to the specified savepoint.
helpviewer_keywords: ["FSCTL_TXFS_SAVEPOINT_INFORMATION","FSCTL_TXFS_SAVEPOINT_INFORMATION control","FSCTL_TXFS_SAVEPOINT_INFORMATION control code [Files]","fs.fsctl_txfs_savepoint_information","winioctl/FSCTL_TXFS_SAVEPOINT_INFORMATION"]
old-location: fs\fsctl_txfs_savepoint_information.htm
tech.root: fs
ms.assetid: 50cf01b4-fd14-4468-9191-79ccd0e2bd05
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_SAVEPOINT_INFORMATION, FSCTL_TXFS_SAVEPOINT_INFORMATION control, FSCTL_TXFS_SAVEPOINT_INFORMATION control code [Files], fs.fsctl_txfs_savepoint_information, winioctl/FSCTL_TXFS_SAVEPOINT_INFORMATION
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
 - FSCTL_TXFS_SAVEPOINT_INFORMATION
 - winioctl/FSCTL_TXFS_SAVEPOINT_INFORMATION
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
 - FSCTL_TXFS_SAVEPOINT_INFORMATION
---

# FSCTL_TXFS_SAVEPOINT_INFORMATION IOCTL


## -description

> [!NOTE]
> Microsoft strongly recommends developers utilize alternative means to achieve your application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](/windows/desktop/FileIO/deprecation-of-txf).

The **FSCTL_TXFS_SAVEPOINT_INFORMATION** control code controls setting, clearing, and rolling back to the specified savepoint.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to resource manager
  FSCTL_TXFS_SAVEPOINT_INFORMATION, // dwIoControlCode
  (LPVOID)lpInBuffer ,              // input buffer
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

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

**ReFS:**  This code is not supported.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [TXFS_SAVEPOINT_INFORMATION](ns-winioctl-txfs_savepoint_information.md)