---
UID: NI:winioctl.IOCTL_SERIAL_LSRMST_INSERT
title: IOCTL_SERIAL_LSRMST_INSERT
description: Enables or disables the placement of line status and modem status values into the regular data stream that an application acquires through the ReadFile function.
helpviewer_keywords: ["IOCTL_SERIAL_LSRMST_INSERT","IOCTL_SERIAL_LSRMST_INSERT control","IOCTL_SERIAL_LSRMST_INSERT control code","_win32_ioctl_serial_lsrmst_insert","base.ioctl_serial_lsrmst_insert","winioctl/IOCTL_SERIAL_LSRMST_INSERT"]
old-location: base\ioctl_serial_lsrmst_insert.htm
tech.root: base
ms.assetid: 9bd427da-1c14-403e-bebe-f64fe4e8723c
ms.date: 12/05/2018
ms.keywords: IOCTL_SERIAL_LSRMST_INSERT, IOCTL_SERIAL_LSRMST_INSERT control, IOCTL_SERIAL_LSRMST_INSERT control code, _win32_ioctl_serial_lsrmst_insert, base.ioctl_serial_lsrmst_insert, winioctl/IOCTL_SERIAL_LSRMST_INSERT
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
 - IOCTL_SERIAL_LSRMST_INSERT
 - winioctl/IOCTL_SERIAL_LSRMST_INSERT
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
 - IOCTL_SERIAL_LSRMST_INSERT
---

# IOCTL_SERIAL_LSRMST_INSERT IOCTL


## -description

Enables or disables the placement of line status and modem status values into the regular data stream that an application acquires through the [ReadFile](../fileapi/nf-fileapi-readfile.md) function.

When this line-status and modem-status data placement mode is enabled, status values are preceded in the data stream by an escape character. The user-definable escape character is set by the **IOCTL_SERIAL_LSRMST_INSERT** control code. See the Remarks section for status value details.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_SERIAL_LSRMST_INSERT,   // dwIoControlCode
  (LPVOID) lpInBuffer,          // input buffer 
  (DWORD) nInBufferSize,        // size of input buffer 
  NULL,                         // lpOutBuffer
  0,                            // nOutBufferSize
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

> [!NOTE]
> An application that uses this scheme must examine each character in the data stream to determine the presence of modem-status or line-status data.

The following values follow the designated escape character in the data stream if the **LSRMST_INSERT** mode has been turned on.

Value | Meaning
------|--------
**SERIAL_LSRMST_ESCAPE** | Indicates the reception of the escape character itself into the data stream.
**SERIAL_LSRMST_LSR_DATA** | Indicates that a line status change occurred, and data was available in the receive hardware buffer. Following this **BYTE** is a **BYTE** value of the line status register is the **BYTE** present in the receive hardware buffer when the line status change was processed.
**SERIAL_LSRMST_LSR_NODATA** | Indicates that a line status change occurred, but no data was available in the receive hardware buffer.
**SERIAL_LSRMST_MST**  | Indicates that a modem status change occurred. Following this **BYTE** is a **BYTE** that is the value of the modem status register when the modem status change was processed.

## -see-also

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md) 