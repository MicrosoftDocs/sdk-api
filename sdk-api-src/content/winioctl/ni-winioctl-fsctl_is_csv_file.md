---
UID: NI:winioctl.FSCTL_IS_CSV_FILE
title: FSCTL_IS_CSV_FILE
description: Determines whether a file is stored on a CSVFS volume, or retrieves namespace information. (FSCTL_IS_CSV_FILE)
helpviewer_keywords: ["FSCTL_IS_CSV_FILE","FSCTL_IS_CSV_FILE control","FSCTL_IS_CSV_FILE control code [Files]","fs.fsctl_is_csv_file","winioctl/FSCTL_IS_CSV_FILE"]
old-location: fs\fsctl_is_csv_file.htm
tech.root: fs
ms.assetid: E2AB8999-7EF5-4F57-BCFB-79FBECE2E998
ms.date: 12/05/2018
ms.keywords: FSCTL_IS_CSV_FILE, FSCTL_IS_CSV_FILE control, FSCTL_IS_CSV_FILE control code [Files], fs.fsctl_is_csv_file, winioctl/FSCTL_IS_CSV_FILE
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
 - FSCTL_IS_CSV_FILE
 - winioctl/FSCTL_IS_CSV_FILE
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
 - FSCTL_IS_CSV_FILE
---

# FSCTL_IS_CSV_FILE IOCTL


## -description

Determines whether a file is stored on a CSVFS volume, or retrieves namespace information.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_IS_CSV_FILE,            // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // lpOutBuffer
  (DWORD) nOutBufferSize,       // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
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

To determine whether a file is stored on a CSVFS volume, simply leave the *lpInBuffer* parameter empty. If the file is on a CSVFS volume, the *lpOutBuffer* parameter will contain **ERROR_SUCCESS**.

To retrieve namespace information, specify a pointer to the same [CSV_NAMESPACE_INFO](ns-winioctl-csv_namespace_info.md) structure that is initially empty (except for the **Version** member) in both the *lpInBuffer* and *lpOutBuffer* parameters. The information in that structure is filled in by the function call.

## -see-also

* [CSV_NAMESPACE_INFO](ns-winioctl-csv_namespace_info.md)
* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)
