---
UID: NS:winioctl.MFT_ENUM_DATA_V1
title: MFT_ENUM_DATA_V1
description: Contains information defining the boundaries for and starting place of an enumeration of update sequence number (USN) change journal records for ReFS volumes.
helpviewer_keywords: ["*PMFT_ENUM_DATA","*PMFT_ENUM_DATA_V1","MFT_ENUM_DATA","MFT_ENUM_DATA_V1","MFT_ENUM_DATA_V1 structure [Files]","PMFT_ENUM_DATA_V1","PMFT_ENUM_DATA_V1 structure pointer [Files]","fs.mft_enum_data_v1","winioctl/MFT_ENUM_DATA_V1","winioctl/PMFT_ENUM_DATA_V1"]
old-location: fs\mft_enum_data_v1.htm
tech.root: fs
ms.assetid: 6d7b50e3-60cf-4eaf-9d22-fbb20c7e0bba
ms.date: 12/05/2018
ms.keywords: '*PMFT_ENUM_DATA, *PMFT_ENUM_DATA_V1, MFT_ENUM_DATA, MFT_ENUM_DATA_V1, MFT_ENUM_DATA_V1 structure [Files], PMFT_ENUM_DATA_V1, PMFT_ENUM_DATA_V1 structure pointer [Files], fs.mft_enum_data_v1, winioctl/MFT_ENUM_DATA_V1, winioctl/PMFT_ENUM_DATA_V1'
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
req.typenames: MFT_ENUM_DATA_V1, *PMFT_ENUM_DATA_V1
req.redist: 
f1_keywords:
 - PMFT_ENUM_DATA_V1
 - winioctl/PMFT_ENUM_DATA_V1
 - MFT_ENUM_DATA_V1
 - winioctl/MFT_ENUM_DATA_V1
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
 - MFT_ENUM_DATA_V1
---

# MFT_ENUM_DATA_V1 structure


## -description

Contains information defining the boundaries for and starting place of an enumeration of update 
    sequence number (USN) change journal records for ReFS volumes. It is used as the input buffer for the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_enum_usn_data">FSCTL_ENUM_USN_DATA</a> control code.

## -struct-fields

### -field StartFileReferenceNumber

The ordinal position within the files on the current volume at which the enumeration is to begin.

The first call to <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_enum_usn_data">FSCTL_ENUM_USN_DATA</a> during an 
       enumeration must have the <b>StartFileReferenceNumber</b> member set to 
       <code>(DWORDLONG)0</code>. Each call to 
       <b>FSCTL_ENUM_USN_DATA</b> retrieves the starting point for 
       the subsequent call as the first entry in the output buffer. Subsequent calls must be made with 
       <b>StartFileReferenceNumber</b> set to this value. For more information, see 
       <b>FSCTL_ENUM_USN_DATA</b>.

### -field LowUsn

The lower boundary of the range of USN values used to filter which records are returned. Only records whose 
      last change journal USN is between or equal to the <b>LowUsn</b> and 
      <b>HighUsn</b> member values are returned.

### -field HighUsn

The upper boundary of the range of USN values used to filter which files are returned.

### -field MinMajorVersion

Indicates the minimum supported major version for the USN change journal.

### -field MaxMajorVersion

Indicates the maximum supported major version for the USN change journal.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The data returned from the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_enum_usn_data">FSCTL_ENUM_USN_DATA</a> 
        control code will contain <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a> 
        structures.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The data returned from the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_enum_usn_data">FSCTL_ENUM_USN_DATA</a> 
        control code will contain <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v2">USN_RECORD_V2</a> or <a href="/windows/desktop/api/winioctl/ns-winioctl-usn_record_v3">USN_RECORD_V3</a> structures.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_enum_usn_data">FSCTL_ENUM_USN_DATA</a>



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>

