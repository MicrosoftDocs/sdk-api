---
UID: NI:winioctl.FSCTL_TXFS_QUERY_RM_INFORMATION
title: FSCTL_TXFS_QUERY_RM_INFORMATION
description: Retrieves information for a resource manager (RM).
helpviewer_keywords: ["FSCTL_TXFS_QUERY_RM_INFORMATION","FSCTL_TXFS_QUERY_RM_INFORMATION control","FSCTL_TXFS_QUERY_RM_INFORMATION control code [Files]","base.fsctl_txfs_query_rm_information","fs.fsctl_txfs_query_rm_information","winioctl/FSCTL_TXFS_QUERY_RM_INFORMATION"]
old-location: fs\fsctl_txfs_query_rm_information.htm
tech.root: fs
ms.assetid: 24e80fdb-9243-455a-a2bf-7bf9b0a61efb
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_QUERY_RM_INFORMATION, FSCTL_TXFS_QUERY_RM_INFORMATION control, FSCTL_TXFS_QUERY_RM_INFORMATION control code [Files], base.fsctl_txfs_query_rm_information, fs.fsctl_txfs_query_rm_information, winioctl/FSCTL_TXFS_QUERY_RM_INFORMATION
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
 - FSCTL_TXFS_QUERY_RM_INFORMATION
 - winioctl/FSCTL_TXFS_QUERY_RM_INFORMATION
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
 - FSCTL_TXFS_QUERY_RM_INFORMATION
---

# FSCTL_TXFS_QUERY_RM_INFORMATION IOCTL


## -description

> [!NOTE]
> Microsoft strongly recommends developers utilize alternative means to achieve your application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](/windows/desktop/FileIO/deprecation-of-txf).

Retrieves information for a resource manager (RM).

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_TXFS_QUERY_RM_INFORMATION,  // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  (LPVOID) lpOutBuffer,             // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
  (LPDWORD) lpBytesReturned,        // bytes returned
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

**FSCTL_TXFS_QUERY_RM_INFORMATION** is a synchronous operation.

If this call fails with **ERROR_BUFFER_TOO_SMALL**, the **BytesRequired** member of the [TXFS_QUERY_RM_INFORMATION](ns-winioctl-txfs_query_rm_information.md) structure specifies how large the buffer must be for the call to return successfully.

If you are writing an application that supports remote Server Message Block Protocol clients, you must use this control code to use the resource manager.

The  resource manager may be queried regardless of its state; if the RM is not started, **ERROR_RM_NOT_ACTIVE** is returned. You can use the information about the active range of the log to guide decisions about how much of the log to archive.

**ReFS:**  This code is not supported.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Secondary Resource Managers for TxF Volumes](/windows/desktop/FileIO/transactional-ntfs-reference)
* [TXFS_QUERY_RM_INFORMATION](ns-winioctl-txfs_query_rm_information.md)