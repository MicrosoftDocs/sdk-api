---
UID: NS:winioctl.USN_JOURNAL_DATA_V1
title: USN_JOURNAL_DATA_V1
description: Represents an update sequence number (USN) change journal, its records, and its capacity.U
helpviewer_keywords: ["*PUSN_JOURNAL_DATA","*PUSN_JOURNAL_DATA_V1","PUSN_JOURNAL_DATA","PUSN_JOURNAL_DATA structure pointer [Files]","PUSN_JOURNAL_DATA_V0","PUSN_JOURNAL_DATA_V0 structure pointer [Files]","USN_JOURNAL_DATA","USN_JOURNAL_DATA structure [Files]","USN_JOURNAL_DATA_V0","USN_JOURNAL_DATA_V0 structure [Files]","USN_JOURNAL_DATA_V1","_win32_usn_journal_data_str","base.usn_journal_data_str","fs.usn_journal_data_str","winioctl/PUSN_JOURNAL_DATA","winioctl/PUSN_JOURNAL_DATA_V0","winioctl/USN_JOURNAL_DATA"]
old-location: fs\usn_journal_data_str.htm
tech.root: fs
ms.assetid: 6b75eab2-aa10-4b48-8918-e4b03b5d8564
ms.date: 12/05/2018
ms.keywords: '*PUSN_JOURNAL_DATA, *PUSN_JOURNAL_DATA_V1, PUSN_JOURNAL_DATA, PUSN_JOURNAL_DATA structure pointer [Files], PUSN_JOURNAL_DATA_V0, PUSN_JOURNAL_DATA_V0 structure pointer [Files], USN_JOURNAL_DATA, USN_JOURNAL_DATA structure [Files], USN_JOURNAL_DATA_V0, USN_JOURNAL_DATA_V0 structure [Files], USN_JOURNAL_DATA_V1, _win32_usn_journal_data_str, base.usn_journal_data_str, fs.usn_journal_data_str, winioctl/PUSN_JOURNAL_DATA, winioctl/PUSN_JOURNAL_DATA_V0, winioctl/USN_JOURNAL_DATA'
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
req.typenames: USN_JOURNAL_DATA_V1, *PUSN_JOURNAL_DATA_V1
req.redist: 
f1_keywords:
 - PUSN_JOURNAL_DATA_V1
 - winioctl/PUSN_JOURNAL_DATA_V1
 - USN_JOURNAL_DATA_V1
 - winioctl/USN_JOURNAL_DATA_V1
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
 - USN_JOURNAL_DATA_V1
---

# USN_JOURNAL_DATA_V1 structure


## -description

Represents an update sequence number (USN) change journal, its records, and its capacity. 
    This structure is the output buffer for the 
    <a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_usn_journal">FSCTL_QUERY_USN_JOURNAL</a> control code. Prior to 
    Windows 8 and Windows Server 2012 this structure was named 
    <b>USN_JOURNAL_DATA</b>. Use that name to compile with older SDKs and 
    compilers.

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

### -field MaxSupportedMajorVersion

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_query_usn_journal">FSCTL_QUERY_USN_JOURNAL</a>



<a href="/windows/desktop/FileIO/volume-management-structures">Volume Management Structures</a>

