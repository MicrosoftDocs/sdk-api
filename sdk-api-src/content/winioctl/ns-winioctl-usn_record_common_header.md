---
UID: NS:winioctl.USN_RECORD_COMMON_HEADER
title: USN_RECORD_COMMON_HEADER
description: Contains the information for an update sequence number (USN) common header which is common through USN_RECORD_V2, USN_RECORD_V3 and USN_RECORD_V4.
helpviewer_keywords: ["*PUSN_RECORD_COMMON_HEADER","PUSN_RECORD_COMMON_HEADER","PUSN_RECORD_COMMON_HEADER structure pointer [Files]","USN_RECORD_COMMON_HEADER","USN_RECORD_COMMON_HEADER structure [Files]","fs.usn_record_common_header","winioctl/PUSN_RECORD_COMMON_HEADER","winioctl/USN_RECORD_COMMON_HEADER"]
old-location: fs\usn_record_common_header.htm
tech.root: fs
ms.assetid: 7B193D8E-FEED-4289-B40F-33BC27889F15
ms.date: 12/05/2018
ms.keywords: '*PUSN_RECORD_COMMON_HEADER, PUSN_RECORD_COMMON_HEADER, PUSN_RECORD_COMMON_HEADER structure pointer [Files], USN_RECORD_COMMON_HEADER, USN_RECORD_COMMON_HEADER structure [Files], fs.usn_record_common_header, winioctl/PUSN_RECORD_COMMON_HEADER, winioctl/USN_RECORD_COMMON_HEADER'
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
req.typenames: USN_RECORD_COMMON_HEADER, *PUSN_RECORD_COMMON_HEADER
req.redist: 
f1_keywords:
 - PUSN_RECORD_COMMON_HEADER
 - winioctl/PUSN_RECORD_COMMON_HEADER
 - USN_RECORD_COMMON_HEADER
 - winioctl/USN_RECORD_COMMON_HEADER
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
 - USN_RECORD_COMMON_HEADER
---

# USN_RECORD_COMMON_HEADER structure


## -description

Contains the information for an update sequence number (USN) common header which is common through <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a>, <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v3">USN_RECORD_V3</a> and [USN_RECORD_V4 structure](ns-winioctl-usn_record_v4.md).

## -struct-fields

### -field RecordLength

The total length of a record, in bytes.

Because USN record is a variable size, the <b>RecordLength</b> member should be used when calculating the address of the next record in an output buffer, for example, a buffer that is returned from operations for the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> function that work with different USN record types.

For [USN_RECORD_V4 structure](ns-winioctl-usn_record_v4.md), the size in bytes of any change journal record is at most the size of the structure, plus (NumberOfExtents-1) times size of the <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_extent">USN_RECORD_EXTENT</a>.

### -field MajorVersion

The major version number of the change journal software for this record.

For example, if the change journal software is version 4.0, the major version number is 4.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>2</td>
<td>The structure is a <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a> structure and the remainder of the structure should be parsed using that layout.</td>
</tr>
<tr>
<td>3</td>
<td>The structure is a <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v3">USN_RECORD_V3</a> structure and the remainder of the structure should be parsed using that layout.</td>
</tr>
<tr>
<td>4</td>
<td>The structure is a [USN_RECORD_V4 structure](ns-winioctl-usn_record_v4.md) and the remainder of the structure should be parsed using that layout.</td>
</tr>
</table>

### -field MinorVersion

The minor version number of the change journal software for this record. For example, if the change journal software is version 4.0, the minor version number is zero.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_extent">USN_RECORD_EXTENT</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v3">USN_RECORD_V3</a>



[USN_RECORD_V4 structure](ns-winioctl-usn_record_v4.md)



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>

