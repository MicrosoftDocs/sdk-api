---
UID: NI:winioctl.IOCTL_SCM_PD_FIRMWARE_ACTIVATE
title: IOCTL_SCM_PD_FIRMWARE_ACTIVATE
description: This is previously available to download firmware to an NVDIMM.
tech.root: FileIO
ms.date: 19/05/2021
ms.keywords: IOCTL_SCM_PD_FIRMWARE_ACTIVATE, IOCTL_SCM_PD_FIRMWARE_ACTIVATE control, IOCTL_SCM_PD_FIRMWARE_ACTIVATE control code [Files], _win32_IOCTL_SCM_PD_FIRMWARE_ACTIVATE, base.IOCTL_SCM_PD_FIRMWARE_ACTIVATE, fs.IOCTL_SCM_PD_FIRMWARE_ACTIVATE, winioctl/IOCTL_SCM_PD_FIRMWARE_ACTIVATE
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
 - IOCTL_SCM_PD_FIRMWARE_ACTIVATE
 - winioctl/IOCTL_SCM_PD_FIRMWARE_ACTIVATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - IOCTL_SCM_PD_FIRMWARE_ACTIVATE
---

# IOCTL_SCM_PD_FIRMWARE_ACTIVATE IOCTL


## -description

This is previously available to activate the downloaded firmware on an NVDIMM. This requires a power cycle to take effect (not runtime activate).

## -ioctlparameters

### -input-buffer

### -input-buffer-length

### -output-buffer

### -output-buffer-length

### -in-out-buffer

### -inout-buffer-length

### -status-block

## -remarks



## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/FileIO/file-management-control-codes">File Management Control Codes</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespacea">GetDiskFreeSpace</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespaceexa">GetDiskFreeSpaceEx</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout">IOCTL_DISK_GET_DRIVE_LAYOUT</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_drive_layout_ex">IOCTL_DISK_GET_DRIVE_LAYOUT_EX</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info">IOCTL_DISK_GET_PARTITION_INFO</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_get_partition_info_ex">IOCTL_DISK_GET_PARTITION_INFO_EX</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>
