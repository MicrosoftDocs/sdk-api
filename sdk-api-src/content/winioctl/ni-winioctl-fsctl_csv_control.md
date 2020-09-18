---
UID: NI:winioctl.FSCTL_CSV_CONTROL
title: FSCTL_CSV_CONTROL
description: Retrieves the results of a CSV control operation.
helpviewer_keywords: ["FSCTL_CSV_CONTROL","FSCTL_CSV_CONTROL control","FSCTL_CSV_CONTROL control code [Files]","fs.fsctl_csv_control","winioctl/FSCTL_CSV_CONTROL"]
old-location: fs\fsctl_csv_control.htm
tech.root: fs
ms.assetid: 6CCCD5CA-FF29-41D4-B687-E403CADABF84
ms.date: 12/05/2018
ms.keywords: FSCTL_CSV_CONTROL, FSCTL_CSV_CONTROL control, FSCTL_CSV_CONTROL control code [Files], fs.fsctl_csv_control, winioctl/FSCTL_CSV_CONTROL
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
 - FSCTL_CSV_CONTROL
 - winioctl/FSCTL_CSV_CONTROL
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
 - FSCTL_CSV_CONTROL
---

# FSCTL_CSV_CONTROL IOCTL


## -description

Retrieves the results of a CSV control operation.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.
 
```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  FSCTL_CSV_CONTROL,            // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer
  (DWORD) nInBufferSize,        // size of input buffer
  (LPVOID) lpOutBuffer,         // output buffer
  (DWORD) nOutBufferSize,       // size of output buffer
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

## -see-also

* [CSV_CONTROL_OP](ne-winioctl-csv_control_op.md)
* [CSV_CONTROL_PARAM](ns-winioctl-csv_control_param.md)
* [CSV_QUERY_FILE_REVISION](ns-winioctl-csv_query_file_revision.md)
* [CSV_QUERY_MDS_PATH](ns-winioctl-csv_query_mds_path.md)
* [CSV_QUERY_REDIRECT_STATE](ns-winioctl-csv_query_redirect_state.md)
* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [File Management Control Codes](/windows/desktop/FileIO/file-management-control-codes)