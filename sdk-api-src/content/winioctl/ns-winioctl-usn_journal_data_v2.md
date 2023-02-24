---
UID: NS:winioctl.USN_JOURNAL_DATA_V2
title: USN_JOURNAL_DATA_V2
description: Represents an update sequence number (USN) change journal, its records, and its capacity. This structure is the output buffer for the FSCTL_QUERY_USN_JOURNAL control code.
helpviewer_keywords: ["*PUSN_JOURNAL_DATA_V2","FLAG_USN_TRACK_MODIFIED_RANGES_ENABLE","PUSN_JOURNAL_DATA_V2","PUSN_JOURNAL_DATA_V2 structure pointer [Files]","USN_JOURNAL_DATA_V2","USN_JOURNAL_DATA_V2 structure [Files]","fs.usn_journal_data_v2","winioctl/PUSN_JOURNAL_DATA_V2","winioctl/USN_JOURNAL_DATA_V2"]
old-location: fs\usn_journal_data_v2.htm
tech.root: fs
ms.assetid: BBFA6D14-1423-45B0-83A0-62019D08507F
ms.date: 12/05/2018
ms.keywords: '*PUSN_JOURNAL_DATA_V2, FLAG_USN_TRACK_MODIFIED_RANGES_ENABLE, PUSN_JOURNAL_DATA_V2, PUSN_JOURNAL_DATA_V2 structure pointer [Files], USN_JOURNAL_DATA_V2, USN_JOURNAL_DATA_V2 structure [Files], fs.usn_journal_data_v2, winioctl/PUSN_JOURNAL_DATA_V2, winioctl/USN_JOURNAL_DATA_V2'
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
req.typenames: USN_JOURNAL_DATA_V2, *PUSN_JOURNAL_DATA_V2
req.redist: 
f1_keywords:
 - PUSN_JOURNAL_DATA_V2
 - winioctl/PUSN_JOURNAL_DATA_V2
 - USN_JOURNAL_DATA_V2
 - winioctl/USN_JOURNAL_DATA_V2
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
 - USN_JOURNAL_DATA_V2
---

# USN_JOURNAL_DATA_V2 structure


## -description

Represents an update sequence number (USN) change journal, its records, and its capacity. This structure is the output buffer for the <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_usn_journal">FSCTL_QUERY_USN_JOURNAL</a> control code.

## -struct-fields

### -field UsnJournalID

The current journal identifier. A journal is assigned a new identifier on creation and can be stamped with 
      a new identifier in the course of its existence. The NTFS file system uses this identifier for an integrity 
      check.

### -field FirstUsn

The number of first record that can be read from the journal.

### -field NextUsn

The number of next record to be written to the journal.

### -field LowestValidUsn

The first record that was written into the journal for this journal instance. Enumerating the files or 
      directories on a volume can return a USN lower than this value (in other words, a 
      <b>FirstUsn</b> member value less than the <b>LowestValidUsn</b> member 
      value). If it does, the journal has been stamped with a new identifier since the last USN was written. In this 
      case, <b>LowestValidUsn</b> may indicate a discontinuity in the journal, in which changes to 
      some or all files or directories on the volume may have occurred that are not recorded in the change 
      journal.

### -field MaxUsn

The largest USN that the change journal supports. An administrator must delete the change journal as the 
      value of <b>NextUsn</b> approaches this value.

### -field MaximumSize

The target maximum size for the change journal, in bytes. The change journal can grow larger than this 
      value, but it is then truncated at the next NTFS file system checkpoint to less than this value.

### -field AllocationDelta

The number of bytes of disk memory added to the end and removed from the beginning of the change journal 
      each time memory is allocated or deallocated. In other words, allocation and deallocation take place in units of 
      this size. An integer multiple of a cluster size is a reasonable value for this member.

### -field MinSupportedMajorVersion

The minimum version of the USN change journal that the file system supports.

### -field MaxSupportedMajorVersion

The maximum version of the USN change journal that the file system supports.

### -field Flags

Whether or not range tracking is turned on. The following are the possible values for the <b>Flags</b> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Range tracking is not turned on for the volume.

</td>
</tr>
<tr>
<td width="40%"><a id="FLAG_USN_TRACK_MODIFIED_RANGES_ENABLE"></a><a id="flag_usn_track_modified_ranges_enable"></a><dl>
<dt><b>FLAG_USN_TRACK_MODIFIED_RANGES_ENABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Range tracking is turned on for the volume.

</td>
</tr>
</table>

### -field RangeTrackChunkSize

The granularity of tracked ranges. Valid only when you also set the <b>Flags</b> member to <b>FLAG_USN_TRACK_MODIFIED_RANGES_ENABLE</b>.

### -field RangeTrackFileSizeThreshold

File size threshold to start tracking range for files with equal or larger size. Valid only when you also set the <b>Flags</b> member to <b>FLAG_USN_TRACK_MODIFIED_RANGES_ENABLE</b>.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_usn_journal">FSCTL_QUERY_USN_JOURNAL</a>



<a href="/windows/desktop/api/winioctl/ns-winioctl-usn_journal_data_v0">USN_JOURNAL_DATA_V0</a>



<a href="/previous-versions/windows/desktop/legacy/hh802707(v=vs.85)">USN_JOURNAL_DATA_V1</a>



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>

