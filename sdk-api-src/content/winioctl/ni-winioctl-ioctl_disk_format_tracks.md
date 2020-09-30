---
UID: NI:winioctl.IOCTL_DISK_FORMAT_TRACKS
title: IOCTL_DISK_FORMAT_TRACKS
description: Formats a specified, contiguous set of tracks on a floppy disk. To provide additional parameters, use IOCTL_DISK_FORMAT_TRACKS_EXinstead.
helpviewer_keywords: ["IOCTL_DISK_FORMAT_TRACKS","IOCTL_DISK_FORMAT_TRACKS control","IOCTL_DISK_FORMAT_TRACKS control code [Files]","_win32_ioctl_disk_format_tracks","base.ioctl_disk_format_tracks","fs.ioctl_disk_format_tracks","winioctl/IOCTL_DISK_FORMAT_TRACKS"]
old-location: fs\ioctl_disk_format_tracks.htm
tech.root: fs
ms.assetid: 9d6e0865-4b4d-4334-855b-3fbd26832591
ms.date: 12/05/2018
ms.keywords: IOCTL_DISK_FORMAT_TRACKS, IOCTL_DISK_FORMAT_TRACKS control, IOCTL_DISK_FORMAT_TRACKS control code [Files], _win32_ioctl_disk_format_tracks, base.ioctl_disk_format_tracks, fs.ioctl_disk_format_tracks, winioctl/IOCTL_DISK_FORMAT_TRACKS
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IOCTL_DISK_FORMAT_TRACKS
 - winioctl/IOCTL_DISK_FORMAT_TRACKS
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
 - IOCTL_DISK_FORMAT_TRACKS
---

# IOCTL_DISK_FORMAT_TRACKS IOCTL


## -description

Formats a specified, contiguous set of tracks on a floppy disk. To provide additional parameters, use [IOCTL_DISK_FORMAT_TRACKS_EX](ni-winioctl-ioctl_disk_format_tracks_ex.md) instead.

To perform this operation, call the [**DeviceIoControl**](../ioapiset/nf-ioapiset-deviceiocontrol.md) function with the following parameters.

```cpp
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_DISK_FORMAT_TRACKS,     // dwIoControlCode
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

* [DeviceIoControl](../ioapiset/nf-ioapiset-deviceiocontrol.md)
* [Disk Management Control Codes](/windows/desktop/FileIO/disk-management-control-codes)
* [FORMAT_PARAMETERS](ns-winioctl-format_parameters.md)
* [IOCTL_DISK_FORMAT_TRACKS_EX](ni-winioctl-ioctl_disk_format_tracks_ex.md)