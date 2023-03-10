---
UID: NI:winioctl.FSCTL_TXFS_WRITE_BACKUP_INFORMATION
title: FSCTL_TXFS_WRITE_BACKUP_INFORMATION
description: Writes Transactional NTFS (TxF) specific information to a specified file.
helpviewer_keywords: ["FSCTL_TXFS_WRITE_BACKUP_INFORMATION","FSCTL_TXFS_WRITE_BACKUP_INFORMATION control","FSCTL_TXFS_WRITE_BACKUP_INFORMATION control code [Files]","fs.fsctl_txfs_write_backup_information","winioctl/FSCTL_TXFS_WRITE_BACKUP_INFORMATION"]
old-location: fs\fsctl_txfs_write_backup_information.htm
tech.root: fs
ms.assetid: 36080d53-9004-40f7-9d92-c6deaac8299f
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_WRITE_BACKUP_INFORMATION, FSCTL_TXFS_WRITE_BACKUP_INFORMATION control, FSCTL_TXFS_WRITE_BACKUP_INFORMATION control code [Files], fs.fsctl_txfs_write_backup_information, winioctl/FSCTL_TXFS_WRITE_BACKUP_INFORMATION
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
 - FSCTL_TXFS_WRITE_BACKUP_INFORMATION
 - winioctl/FSCTL_TXFS_WRITE_BACKUP_INFORMATION
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
 - FSCTL_TXFS_WRITE_BACKUP_INFORMATION
---

# FSCTL_TXFS_WRITE_BACKUP_INFORMATION IOCTL


## -description

> [!NOTE]
> Microsoft strongly recommends developers utilize alternative means to achieve your application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](/windows/desktop/FileIO/deprecation-of-txf).

Writes  Transactional NTFS (TxF) specific information to a specified file. The **Buffer** member of the [TXFS_WRITE_BACKUP_INFORMATION](ns-winioctl-txfs_write_backup_information.md) structure must be the **Buffer** member of the [TXFS_READ_BACKUP_INFORMATION_OUT](ns-winioctl-txfs_read_backup_information_out.md) structure returned by [FSCTL_TXFS_READ_BACKUP_INFORMATION](ni-winioctl-fsctl_txfs_read_backup_information.md).

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                     // handle to device
  FSCTL_TXFS_WRITE_BACKUP_INFORMATION,  // dwIoControlCode
  (LPVOID) lpInBuffer,                  // input buffer
  (DWORD) nInBufferSize,                // size of input buffer
  NULL,                                 // lpOutBuffer
  0,                                    // nOutBufferSize
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

**FSCTL_TXFS_WRITE_BACKUP_INFORMATION** is a synchronous operation.

This control code can be used by backup functions and applications, such as Win32 [BackupRead](../winbase/nf-winbase-backupread.md), and by Volume Snapshot Service (VSS) writers that support secondary resource managers. For more information, see [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service).

**ReFS:**  This code is not supported.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FSCTL_TXFS_READ_BACKUP_INFORMATION](ni-winioctl-fsctl_txfs_read_backup_information.md)
* [TXFS_WRITE_BACKUP_INFORMATION](ns-winioctl-txfs_write_backup_information.md)
* [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service)