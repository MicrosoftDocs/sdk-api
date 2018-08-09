---
UID: NS:winioctl.USN_TRACK_MODIFIED_RANGES
title: USN_TRACK_MODIFIED_RANGES
author: windows-sdk-content
description: Contains information on range tracking parameters for an update sequence number (USN) change journal using the FSCTL_USN_TRACK_MODIFIED_RANGES control code.
old-location: fs\usn_track_modified_ranges.htm
old-project: fileio
ms.assetid: 00254BBD-8F38-46AB-8B0A-3094020A48C5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PUSN_TRACK_MODIFIED_RANGES, PUSN_TRACK_MODIFIED_RANGES, PUSN_TRACK_MODIFIED_RANGES structure pointer [Files], USN_TRACK_MODIFIED_RANGES, USN_TRACK_MODIFIED_RANGES structure [Files], fs.usn_track_modified_ranges, winioctl/PUSN_TRACK_MODIFIED_RANGES, winioctl/USN_TRACK_MODIFIED_RANGES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: USN_TRACK_MODIFIED_RANGES, *PUSN_TRACK_MODIFIED_RANGES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - USN_TRACK_MODIFIED_RANGES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# USN_TRACK_MODIFIED_RANGES structure


## -description


Contains information on range tracking parameters for an update sequence number (USN) change journal using the <a href="https://msdn.microsoft.com/258E16B2-B6E8-44BB-8073-B1BEDD4FA86A">FSCTL_USN_TRACK_MODIFIED_RANGES</a> control code.


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
<td>This flag is mandatory with <a href="https://msdn.microsoft.com/258E16B2-B6E8-44BB-8073-B1BEDD4FA86A">FSCTL_USN_TRACK_MODIFIED_RANGES</a> and is used to enable range tracking on the volume.</td>
</tr>
</table>
 


### -field Unused

Reserved.


### -field ChunkSize

Chunk size for tracking ranges. A single byte modification will be reflected as the whole chunk being modified.


### -field FileSizeThreshold

File size threshold to start outputting <a href="https://msdn.microsoft.com/2636D1A1-6FD1-4F84-954C-499DCCE6E390">USN_RECORD_V4</a> record(s) for modified file, i.e. if the modified file size is less than this threshold, then no <b>USN_RECORD_V4</b> record will be output. 


## -remarks



Once range tracking is enabled for a given volume it cannot be disabled except by deleting the USN Journal and recreating it.




## -see-also




<a href="https://msdn.microsoft.com/258E16B2-B6E8-44BB-8073-B1BEDD4FA86A">FSCTL_USN_TRACK_MODIFIED_RANGES</a>
 

 

