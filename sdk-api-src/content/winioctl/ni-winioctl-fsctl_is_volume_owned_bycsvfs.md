---
UID: NI:winioctl.FSCTL_IS_VOLUME_OWNED_BYCSVFS
title: FSCTL_IS_VOLUME_OWNED_BYCSVFS
description: Determines whether a volume is locked by CSVFS.
helpviewer_keywords: ["FSCTL_IS_VOLUME_OWNED_BYCSVFS","FSCTL_IS_VOLUME_OWNED_BYCSVFS control","FSCTL_IS_VOLUME_OWNED_BYCSVFS control code [Files]","fs.fsctl_is_volume_owned_bycsvfs","winioctl/FSCTL_IS_VOLUME_OWNED_BYCSVFS"]
old-location: fs\fsctl_is_volume_owned_bycsvfs.htm
tech.root: fs
ms.assetid: AA9D31DD-352C-4509-A5F3-55DC1C685E33
ms.date: 12/05/2018
ms.keywords: FSCTL_IS_VOLUME_OWNED_BYCSVFS, FSCTL_IS_VOLUME_OWNED_BYCSVFS control, FSCTL_IS_VOLUME_OWNED_BYCSVFS control code [Files], fs.fsctl_is_volume_owned_bycsvfs, winioctl/FSCTL_IS_VOLUME_OWNED_BYCSVFS
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - FSCTL_IS_VOLUME_OWNED_BYCSVFS
 - winioctl/FSCTL_IS_VOLUME_OWNED_BYCSVFS
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
 - FSCTL_IS_VOLUME_OWNED_BYCSVFS
---

# FSCTL_IS_VOLUME_OWNED_BYCSVFS IOCTL


## -description

Determines whether a volume is locked by CSVFS.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                 // handle to device
  FSCTL_IS_VOLUME_OWNED_BYCSVFS,    // dwIoControlCode
  NULL,                             // input buffer
  0,                                // size of input buffer
  (LPVOID) lpOutBuffer,             // lpOutBuffer
  (DWORD) nOutBufferSize,           // nOutBufferSize
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

If the volume is locked on behalf of CSVFS, the control code returns information that is sent to an NTFS volume. If the volume is locked (using [FSCTL_LOCK_VOLUME](ni-winioctl-fsctl_lock_volume.md)) from a request that originates from CSVFS, then the [CSV_IS_OWNED_BY_CSVFS](ns-winioctl-csv_is_owned_by_csvfs.md) structure's **OwnedByCSVFS** member has a value of **TRUE**.

## -see-also

* [CSV_IS_OWNED_BY_CSVFS](ns-winioctl-csv_is_owned_by_csvfs.md)
* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)