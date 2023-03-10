---
UID: NS:winioctl.USN_TRACK_MODIFIED_RANGES
title: USN_TRACK_MODIFIED_RANGES
description: Contains information on range tracking parameters for an update sequence number (USN) change journal using the FSCTL_USN_TRACK_MODIFIED_RANGES control code.
helpviewer_keywords: ["*PUSN_TRACK_MODIFIED_RANGES","PUSN_TRACK_MODIFIED_RANGES","PUSN_TRACK_MODIFIED_RANGES structure pointer [Files]","USN_TRACK_MODIFIED_RANGES","USN_TRACK_MODIFIED_RANGES structure [Files]","fs.usn_track_modified_ranges","winioctl/PUSN_TRACK_MODIFIED_RANGES","winioctl/USN_TRACK_MODIFIED_RANGES"]
old-location: fs\usn_track_modified_ranges.htm
tech.root: fs
ms.assetid: 00254BBD-8F38-46AB-8B0A-3094020A48C5
ms.date: 12/05/2018
ms.keywords: '*PUSN_TRACK_MODIFIED_RANGES, PUSN_TRACK_MODIFIED_RANGES, PUSN_TRACK_MODIFIED_RANGES structure pointer [Files], USN_TRACK_MODIFIED_RANGES, USN_TRACK_MODIFIED_RANGES structure [Files], fs.usn_track_modified_ranges, winioctl/PUSN_TRACK_MODIFIED_RANGES, winioctl/USN_TRACK_MODIFIED_RANGES'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: USN_TRACK_MODIFIED_RANGES, *PUSN_TRACK_MODIFIED_RANGES
req.redist: 
f1_keywords:
 - PUSN_TRACK_MODIFIED_RANGES
 - winioctl/PUSN_TRACK_MODIFIED_RANGES
 - USN_TRACK_MODIFIED_RANGES
 - winioctl/USN_TRACK_MODIFIED_RANGES
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
 - USN_TRACK_MODIFIED_RANGES
---

# USN_TRACK_MODIFIED_RANGES structure


## -description

Contains information on range tracking parameters for an update sequence number (USN) change journal using the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_usn_track_modified_ranges">FSCTL_USN_TRACK_MODIFIED_RANGES</a> control code.

## -struct-fields

### -field Flags

Indicates enabling range tracking.

<table>
<tr>
<td>Value</td>
<td>Description</td>
</tr>
<tr>
<td>FLAG_USN_TRACK_MODIFIED_RANGES_ENABLE 
0x00000001 
</td>
<td>This flag is mandatory with <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_usn_track_modified_ranges">FSCTL_USN_TRACK_MODIFIED_RANGES</a> and is used to enable range tracking on the volume.</td>
</tr>
</table>

### -field Unused

Reserved.

### -field ChunkSize

Chunk size for tracking ranges. A single byte modification will be reflected as the whole chunk being modified.

### -field FileSizeThreshold

File size threshold to start outputting [USN_RECORD_V4 structure](ns-winioctl-usn_record_v4.md) record(s) for modified file, i.e. if the modified file size is less than this threshold, then no <b>USN_RECORD_V4</b> record will be output.

## -remarks

Once range tracking is enabled for a given volume it cannot be disabled except by deleting the USN Journal and recreating it.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_usn_track_modified_ranges">FSCTL_USN_TRACK_MODIFIED_RANGES</a>

