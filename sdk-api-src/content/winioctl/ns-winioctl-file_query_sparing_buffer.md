---
UID: NS:winioctl._FILE_QUERY_SPARING_BUFFER
title: FILE_QUERY_SPARING_BUFFER
description: Contains defect management properties.
helpviewer_keywords: ["*PFILE_QUERY_SPARING_BUFFER","FILE_QUERY_SPARING_BUFFER","FILE_QUERY_SPARING_BUFFER structure [Files]","PFILE_QUERY_SPARING_BUFFER","PFILE_QUERY_SPARING_BUFFER structure pointer [Files]","fs.file_query_sparing_buffer","winioctl/FILE_QUERY_SPARING_BUFFER","winioctl/PFILE_QUERY_SPARING_BUFFER"]
old-location: fs\file_query_sparing_buffer.htm
tech.root: fs
ms.assetid: 4b9b44ec-9e8e-4ebd-b192-952bbb71005d
ms.date: 12/05/2018
ms.keywords: '*PFILE_QUERY_SPARING_BUFFER, FILE_QUERY_SPARING_BUFFER, FILE_QUERY_SPARING_BUFFER structure [Files], PFILE_QUERY_SPARING_BUFFER, PFILE_QUERY_SPARING_BUFFER structure pointer [Files], fs.file_query_sparing_buffer, winioctl/FILE_QUERY_SPARING_BUFFER, winioctl/PFILE_QUERY_SPARING_BUFFER'
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
req.typenames: FILE_QUERY_SPARING_BUFFER, *PFILE_QUERY_SPARING_BUFFER
req.redist: 
f1_keywords:
 - _FILE_QUERY_SPARING_BUFFER
 - winioctl/_FILE_QUERY_SPARING_BUFFER
 - PFILE_QUERY_SPARING_BUFFER
 - winioctl/PFILE_QUERY_SPARING_BUFFER
 - FILE_QUERY_SPARING_BUFFER
 - winioctl/FILE_QUERY_SPARING_BUFFER
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
 - FILE_QUERY_SPARING_BUFFER
---

# FILE_QUERY_SPARING_BUFFER structure


## -description

Contains   defect management properties.

## -struct-fields

### -field SparingUnitBytes

The size of a sparing packet and the underlying error check and correction (ECC) block size of the volume.

### -field SoftwareSparing

If <b>TRUE</b>, indicates that sparing behavior is software-based; if <b>FALSE</b>, it is hardware-based.

### -field TotalSpareBlocks

The total number of blocks allocated for sparing.

### -field FreeSpareBlocks

The  number of blocks available for sparing.

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_sparing_info">FSCTL_QUERY_SPARING_INFO</a>