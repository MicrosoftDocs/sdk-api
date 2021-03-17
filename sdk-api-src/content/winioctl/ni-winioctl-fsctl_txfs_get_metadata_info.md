---
UID: NI:winioctl.FSCTL_TXFS_GET_METADATA_INFO
title: FSCTL_TXFS_GET_METADATA_INFO
description: Retrieves Transacted NTFS (TxF) metadata for a file and the GUID of the transaction that has locked the specified file (if the file is locked).
helpviewer_keywords: ["FSCTL_TXFS_GET_METADATA_INFO","FSCTL_TXFS_GET_METADATA_INFO control","FSCTL_TXFS_GET_METADATA_INFO control code [Files]","fs.fsctl_txfs_get_metadata_info","winioctl/FSCTL_TXFS_GET_METADATA_INFO"]
old-location: fs\fsctl_txfs_get_metadata_info.htm
tech.root: fs
ms.assetid: 129e682c-bc95-46d5-a0d3-adbadc7e6478
ms.date: 12/05/2018
ms.keywords: FSCTL_TXFS_GET_METADATA_INFO, FSCTL_TXFS_GET_METADATA_INFO control, FSCTL_TXFS_GET_METADATA_INFO control code [Files], fs.fsctl_txfs_get_metadata_info, winioctl/FSCTL_TXFS_GET_METADATA_INFO
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
 - FSCTL_TXFS_GET_METADATA_INFO
 - winioctl/FSCTL_TXFS_GET_METADATA_INFO
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
 - FSCTL_TXFS_GET_METADATA_INFO
---

# FSCTL_TXFS_GET_METADATA_INFO IOCTL


## -description

> [!NOTE]
> Microsoft strongly recommends developers utilize alternative means to achieve your application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](/windows/desktop/FileIO/deprecation-of-txf).

Retrieves Transacted NTFS (TxF) metadata for a file and the <b>GUID</b> of the transaction that has locked the specified file (if the file is locked). 

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_TXFS_GET_METADATA_INFO,     // dwIoControlCode
  NULL,                             // lpInBuffer
  0,                                // nInBufferSize
  (LPVOID) lpOutBuffer,             // output buffer
  (DWORD) nOutBufferSize,           // size of output buffer
  (LPDWORD) lpBytesReturned,        // number of bytes returned
  NULL                              // OVERLAPPED structure
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

**FSCTL_TXFS_GET_METADATA_INFO** is a synchronous operation.

**ReFS:**  This code is not supported.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [TXFS_GET_METADATA_INFO_OUT](ns-winioctl-txfs_get_metadata_info_out.md)