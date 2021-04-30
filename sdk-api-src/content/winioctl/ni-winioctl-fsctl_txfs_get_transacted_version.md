---
UID: NI:winioctl.FSCTL_TXFS_GET_TRANSACTED_VERSION
title: FSCTL_TXFS_GET_TRANSACTED_VERSION
description: Returns a TXFS_GET_TRANSACTED_VERSION structure. The structure identifies the most recently committed version of the specified file, the version number of the handle.
helpviewer_keywords: ["FSCTL_TXFS_GET_TRANSACTED_VERSION","FSCTL_TXFS_GET_TRANSACTED_VERSION control","FSCTL_TXFS_GET_TRANSACTED_VERSION control code [Files]","fs.fsctl_txfs_get_transacted_version","winioctl/FSCTL_TXFS_GET_TRANSACTED_VERSION"]
old-location: fs\fsctl_txfs_get_transacted_version.htm
tech.root: fs
ms.assetid: 71864348-1266-4ac5-a4b5-b9aaff52b0c5
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_GET_TRANSACTED_VERSION, FSCTL_TXFS_GET_TRANSACTED_VERSION control, FSCTL_TXFS_GET_TRANSACTED_VERSION control code [Files], fs.fsctl_txfs_get_transacted_version, winioctl/FSCTL_TXFS_GET_TRANSACTED_VERSION
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
 - FSCTL_TXFS_GET_TRANSACTED_VERSION
 - winioctl/FSCTL_TXFS_GET_TRANSACTED_VERSION
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
 - FSCTL_TXFS_GET_TRANSACTED_VERSION
---

# FSCTL_TXFS_GET_TRANSACTED_VERSION IOCTL


## -description

> [!NOTE]
> Microsoft strongly recommends developers utilize alternative means to achieve your application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](/windows/desktop/FileIO/deprecation-of-txf).

Returns a [TXFS_GET_TRANSACTED_VERSION](ns-winioctl-txfs_get_transacted_version.md) structure.  The structure identifies the most recently committed version of the specified file, the version number of the handle. 

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                     // handle to device
  FSCTL_TXFS_GET_TRANSACTED_VERSION,    // dwIoControlCode
  NULL,                                 // lpInBuffer
  0,                                    // nInBufferSize
  (LPVOID) lpOutBuffer,                 // output buffer
  (DWORD) nOutBufferSize,               // size of output buffer
  (LPDWORD) lpBytesReturned,            // number of bytes returned
  NULL                                  // OVERLAPPED structure
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

**FSCTL_TXFS_GET_TRANSACTED_VERSION** is a synchronous operation.

This control code can be use to track the latest version of a base file. For a specified handle, the base version is always the base value returned when the handle was opened, but the latest version changes based on any commit operations another transaction makes.  If handle is then closed and opened again, base version and latest version are updated to new values and any subsequent commit operations from the other transaction change the latest version.

If you attempt to retrieve the version of a resource manager's root, the value **TXFS_TRANSACTED_VERSION_NONTRANSACTED** is returned.

**ReFS:**  This code is not supported.

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [TXFS_GET_TRANSACTED_VERSION](ns-winioctl-txfs_get_transacted_version.md)