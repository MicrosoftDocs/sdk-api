---
UID: NS:winioctl.USN_RANGE_TRACK_OUTPUT
title: USN_RANGE_TRACK_OUTPUT
description: Contains returned update sequence number (USN) from FSCTL_USN_TRACK_MODIFIED_RANGES control code.
helpviewer_keywords: ["*PUSN_RANGE_TRACK_OUTPUT","PUSN_RANGE_TRACK_OUTPUT","PUSN_RANGE_TRACK_OUTPUT structure pointer [Files]","USN_RANGE_TRACK_OUTPUT","USN_RANGE_TRACK_OUTPUT structure [Files]","fs.usn_range_track_output","winioctl/PUSN_RANGE_TRACK_OUTPUT","winioctl/USN_RANGE_TRACK_OUTPUT"]
old-location: fs\usn_range_track_output.htm
tech.root: fs
ms.assetid: E10ECB50-A506-4836-81D2-3073FBB844CA
ms.date: 12/05/2018
ms.keywords: '*PUSN_RANGE_TRACK_OUTPUT, PUSN_RANGE_TRACK_OUTPUT, PUSN_RANGE_TRACK_OUTPUT structure pointer [Files], USN_RANGE_TRACK_OUTPUT, USN_RANGE_TRACK_OUTPUT structure [Files], fs.usn_range_track_output, winioctl/PUSN_RANGE_TRACK_OUTPUT, winioctl/USN_RANGE_TRACK_OUTPUT'
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
req.typenames: USN_RANGE_TRACK_OUTPUT, *PUSN_RANGE_TRACK_OUTPUT
req.redist: 
f1_keywords:
 - PUSN_RANGE_TRACK_OUTPUT
 - winioctl/PUSN_RANGE_TRACK_OUTPUT
 - USN_RANGE_TRACK_OUTPUT
 - winioctl/USN_RANGE_TRACK_OUTPUT
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
 - USN_RANGE_TRACK_OUTPUT
---

# USN_RANGE_TRACK_OUTPUT structure


## -description

Contains returned update sequence number (USN) from <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_usn_track_modified_ranges">FSCTL_USN_TRACK_MODIFIED_RANGES</a> control code.

## -struct-fields

### -field Usn

Returned update sequence number (USN) that identifies at what point in the USN Journal that range tracking was enabled.

## -remarks

This structure is optional.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_usn_track_modified_ranges">FSCTL_USN_TRACK_MODIFIED_RANGES</a>

