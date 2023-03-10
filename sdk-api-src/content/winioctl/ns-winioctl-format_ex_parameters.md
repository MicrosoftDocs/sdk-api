---
UID: NS:winioctl._FORMAT_EX_PARAMETERS
title: FORMAT_EX_PARAMETERS
description: Contains information used in formatting a contiguous set of disk tracks. It is used by the IOCTL_DISK_FORMAT_TRACKS_EX control code.
helpviewer_keywords: ["*PFORMAT_EX_PARAMETERS","FORMAT_EX_PARAMETERS","FORMAT_EX_PARAMETERS structure [Files]","PFORMAT_EX_PARAMETERS","PFORMAT_EX_PARAMETERS structure pointer [Files]","_win32_format_ex_parameters_str","base.format_ex_parameters_str","fs.format_ex_parameters_str","winioctl/FORMAT_EX_PARAMETERS","winioctl/PFORMAT_EX_PARAMETERS"]
old-location: fs\format_ex_parameters_str.htm
tech.root: fs
ms.assetid: e508106c-a77a-476f-ba71-ea8f9a2d94d6
ms.date: 12/05/2018
ms.keywords: '*PFORMAT_EX_PARAMETERS, FORMAT_EX_PARAMETERS, FORMAT_EX_PARAMETERS structure [Files], PFORMAT_EX_PARAMETERS, PFORMAT_EX_PARAMETERS structure pointer [Files], _win32_format_ex_parameters_str, base.format_ex_parameters_str, fs.format_ex_parameters_str, winioctl/FORMAT_EX_PARAMETERS, winioctl/PFORMAT_EX_PARAMETERS'
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
req.typenames: FORMAT_EX_PARAMETERS, *PFORMAT_EX_PARAMETERS
req.redist: 
f1_keywords:
 - _FORMAT_EX_PARAMETERS
 - winioctl/_FORMAT_EX_PARAMETERS
 - PFORMAT_EX_PARAMETERS
 - winioctl/PFORMAT_EX_PARAMETERS
 - FORMAT_EX_PARAMETERS
 - winioctl/FORMAT_EX_PARAMETERS
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
 - FORMAT_EX_PARAMETERS
---

# FORMAT_EX_PARAMETERS structure


## -description

Contains information used in formatting a contiguous set of disk tracks. It is used by the 
<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_format_tracks_ex">IOCTL_DISK_FORMAT_TRACKS_EX</a> control code.

## -struct-fields

### -field MediaType

The media type. For a list of values, see 
<a href="/windows/desktop/api/winioctl/ne-winioctl-media_type">MEDIA_TYPE</a>.

### -field StartCylinderNumber

The cylinder number at which to begin the format.

### -field EndCylinderNumber

The cylinder number at which to end the format.

### -field StartHeadNumber

The beginning head location.

### -field EndHeadNumber

The ending head location.

### -field FormatGapLength

The length of the gap between two successive sectors on a track.

### -field SectorsPerTrack

The number of sectors in each track.

### -field SectorNumber

An array of values specifying the sector numbers of the sectors to be included in the track to be formatted.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_format_tracks_ex">IOCTL_DISK_FORMAT_TRACKS_EX</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-media_type">MEDIA_TYPE</a>