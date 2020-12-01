---
UID: NI:winioctl.FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS
title: FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS
description: Retrieves information about a file system for which CSVFS is a proxy.
helpviewer_keywords: ["FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS","FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS control","FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS control code [Files]","fs.fsctl_csv_query_down_level_file_system_characteristics","winioctl/FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS"]
old-location: fs\fsctl_csv_query_down_level_file_system_characteristics.htm
tech.root: fs
ms.assetid: 1AC3FD47-70B8-4735-9B25-A8B2BAEE5A83
ms.date: 12/05/2018
ms.keywords: FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS, FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS control, FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS control code [Files], fs.fsctl_csv_query_down_level_file_system_characteristics, winioctl/FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS
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
 - FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS
 - winioctl/FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS
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
 - FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS
---

# FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS IOCTL


## -description

Retrieves information about a file system for which CSVFS is a proxy.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,                                       // handle to device
  FSCTL_CSV_QUERY_DOWN_LEVEL_FILE_SYSTEM_CHARACTERISTICS, // dwIoControlCode
  NULL,                                                   // input buffer
  0,                                                      // size of input buffer
  (LPVOID) lpOutBuffer,                                   // lpOutBuffer
  (DWORD) nOutBufferSize,                                 // nOutBufferSize
  (LPDWORD) lpBytesReturned,                              // number of bytes returned
  (LPOVERLAPPED) lpOverlapped                             // OVERLAPPED structure
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

## -see-also

* [CreateFile](../fileapi/nf-fileapi-createfilea.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [FILE_FS_ATTRIBUTE_INFORMATION](/windows-hardware/drivers/ddi/content/ntifs/ns-ntifs-_file_fs_attribute_information)
* [Volume Management Control Codes](/windows/desktop/FileIO/volume-management-control-codes)