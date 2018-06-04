---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# USN_JOURNAL_DATA_V2 structure


## -description


Represents an update sequence number (USN) change journal, its records, and its capacity. This structure is the output buffer for the <a href="https://msdn.microsoft.com/9491b054-934a-4b76-bf77-f397b6386f82">FSCTL_QUERY_USN_JOURNAL</a> control code.


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




<a href="https://msdn.microsoft.com/9491b054-934a-4b76-bf77-f397b6386f82">FSCTL_QUERY_USN_JOURNAL</a>



<a href="https://msdn.microsoft.com/6b75eab2-aa10-4b48-8918-e4b03b5d8564">USN_JOURNAL_DATA_V0</a>



<a href="https://msdn.microsoft.com/3ee0a76e-848c-4f41-9e8b-1ff023c7f3b3">USN_JOURNAL_DATA_V1</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

