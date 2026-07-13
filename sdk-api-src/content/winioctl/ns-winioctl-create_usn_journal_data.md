---
UID: NS:winioctl.CREATE_USN_JOURNAL_DATA
title: CREATE_USN_JOURNAL_DATA
description: Contains information that describes an update sequence number (USN) change journal.
helpviewer_keywords: ["*PCREATE_USN_JOURNAL_DATA","CREATE_USN_JOURNAL_DATA","CREATE_USN_JOURNAL_DATA structure [Files]","PCREATE_USN_JOURNAL_DATA","PCREATE_USN_JOURNAL_DATA structure pointer [Files]","_win32_create_usn_journal_data_str","base.create_usn_journal_data_str","fs.create_usn_journal_data_str","winioctl/CREATE_USN_JOURNAL_DATA","winioctl/PCREATE_USN_JOURNAL_DATA"]
old-location: fs\create_usn_journal_data_str.htm
tech.root: fs
ms.assetid: 84d00427-c6eb-41aa-a594-8c57bdd56202
ms.date: 12/05/2018
ms.keywords: '*PCREATE_USN_JOURNAL_DATA, CREATE_USN_JOURNAL_DATA, CREATE_USN_JOURNAL_DATA structure [Files], PCREATE_USN_JOURNAL_DATA, PCREATE_USN_JOURNAL_DATA structure pointer [Files], _win32_create_usn_journal_data_str, base.create_usn_journal_data_str, fs.create_usn_journal_data_str, winioctl/CREATE_USN_JOURNAL_DATA, winioctl/PCREATE_USN_JOURNAL_DATA'
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
req.typenames: CREATE_USN_JOURNAL_DATA, *PCREATE_USN_JOURNAL_DATA
req.redist: 
f1_keywords:
 - PCREATE_USN_JOURNAL_DATA
 - winioctl/PCREATE_USN_JOURNAL_DATA
 - CREATE_USN_JOURNAL_DATA
 - winioctl/CREATE_USN_JOURNAL_DATA
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
 - CREATE_USN_JOURNAL_DATA
---

# CREATE_USN_JOURNAL_DATA structure


## -description

Contains information that describes an update sequence number (USN) change journal.

## -struct-fields

### -field MaximumSize

The target maximum size that the NTFS file system allocates for the change journal, in bytes.

The change journal can grow larger than this value, but it is then truncated at the next NTFS file system 
       checkpoint to less than this value.

### -field AllocationDelta

The size of memory allocation that is added to the end and removed from the beginning of the change journal, in bytes.

The change journal can grow to more than the sum of the values of <b>MaximumSize</b> and 
       <b>AllocationDelta</b> before being trimmed.

## -remarks

For more information, see 
    <a href="/windows/desktop/FileIO/creating-modifying-and-deleting-a-change-journal">Creating, Modifying, and Deleting a Change Journal</a>.

## -see-also

<a href="/windows/desktop/api/winioctl/ni-winioctl-fsctl_create_usn_journal">FSCTL_CREATE_USN_JOURNAL</a>

