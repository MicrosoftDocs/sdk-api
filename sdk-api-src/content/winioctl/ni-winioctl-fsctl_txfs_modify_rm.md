---
UID: NI:winioctl.FSCTL_TXFS_MODIFY_RM
title: FSCTL_TXFS_MODIFY_RM
description: Sets the log mode and log parameter information for a secondary resource manager (RM).
helpviewer_keywords: ["FSCTL_TXFS_MODIFY_RM","FSCTL_TXFS_MODIFY_RM control","FSCTL_TXFS_MODIFY_RM control code [Files]","base.fsctl_txfs_set_rm_information","fs.fsctl_txfs_modify_rm","fs.fsctl_txfs_set_rm_information","winioctl/FSCTL_TXFS_MODIFY_RM"]
old-location: fs\fsctl_txfs_modify_rm.htm
tech.root: fs
ms.assetid: 29054321-a805-4a4e-90fb-a5b8e2858da0
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_MODIFY_RM, FSCTL_TXFS_MODIFY_RM control, FSCTL_TXFS_MODIFY_RM control code [Files], base.fsctl_txfs_set_rm_information, fs.fsctl_txfs_modify_rm, fs.fsctl_txfs_set_rm_information, winioctl/FSCTL_TXFS_MODIFY_RM
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
 - FSCTL_TXFS_MODIFY_RM
 - winioctl/FSCTL_TXFS_MODIFY_RM
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
 - FSCTL_TXFS_MODIFY_RM
---

# FSCTL_TXFS_MODIFY_RM IOCTL


## -description

> [!NOTE]
> Microsoft strongly recommends developers utilize alternative means to achieve your application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](/windows/desktop/FileIO/deprecation-of-txf).

Sets the log mode and log parameter information for a secondary resource manager (RM).

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_TXFS_MODIFY_RM,         // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  NULL,                         // lpOutBuffer
  0,                            // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // bytes returned
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

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -remarks

**FSCTL_TXFS_MODIFY_RM** is a synchronous operation.

This control code is for remote clients to use when setting log parameters, and for local clients to specify log parameters for the default RMs.

<div class="alert"><b>Note</b>  You cannot set the logging mode for a default RM. The logging mode for a default RM is 
     <b>TXFS_LOGGING_MODE_SIMPLE</b>.</div>
<div> </div>

**ReFS:**  This code is not supported.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Secondary Resource Managers for TxF Volumes](/windows/desktop/FileIO/transactional-ntfs-reference)
* [TXFS_MODIFY_RM](ns-winioctl-txfs_modify_rm.md)