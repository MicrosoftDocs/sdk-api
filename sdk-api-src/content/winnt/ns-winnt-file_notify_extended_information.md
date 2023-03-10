---
UID: NS:winnt._FILE_NOTIFY_EXTENDED_INFORMATION
title: FILE_NOTIFY_EXTENDED_INFORMATION (winnt.h)
description: Describes the changes found by the ReadDirectoryChangesExW function.
helpviewer_keywords: ["*PFILE_NOTIFY_EXTENDED_INFORMATION","FILE_ACTION_ADDED","FILE_ACTION_MODIFIED","FILE_ACTION_REMOVED","FILE_ACTION_RENAMED_NEW_NAME","FILE_ACTION_RENAMED_OLD_NAME","FILE_NOTIFY_EXTENDED_INFORMATION","FILE_NOTIFY_EXTENDED_INFORMATION structure [Files]","PFILE_NOTIFY_EXTENDED_INFORMATION","PFILE_NOTIFY_EXTENDED_INFORMATION structure pointer [Files]","fs.file_notify_extended_information","winnt/FILE_NOTIFY_EXTENDED_INFORMATION","winnt/PFILE_NOTIFY_EXTENDED_INFORMATION"]
old-location: fs\file_notify_extended_information.htm
tech.root: fs
ms.assetid: 4558F2E8-F515-4202-9CAA-FDAF20160F61
ms.date: 12/05/2018
ms.keywords: '*PFILE_NOTIFY_EXTENDED_INFORMATION, FILE_ACTION_ADDED, FILE_ACTION_MODIFIED, FILE_ACTION_REMOVED, FILE_ACTION_RENAMED_NEW_NAME, FILE_ACTION_RENAMED_OLD_NAME, FILE_NOTIFY_EXTENDED_INFORMATION, FILE_NOTIFY_EXTENDED_INFORMATION structure [Files], PFILE_NOTIFY_EXTENDED_INFORMATION, PFILE_NOTIFY_EXTENDED_INFORMATION structure pointer [Files], fs.file_notify_extended_information, winnt/FILE_NOTIFY_EXTENDED_INFORMATION, winnt/PFILE_NOTIFY_EXTENDED_INFORMATION'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: FILE_NOTIFY_EXTENDED_INFORMATION, *PFILE_NOTIFY_EXTENDED_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILE_NOTIFY_EXTENDED_INFORMATION
 - winnt/_FILE_NOTIFY_EXTENDED_INFORMATION
 - PFILE_NOTIFY_EXTENDED_INFORMATION
 - winnt/PFILE_NOTIFY_EXTENDED_INFORMATION
 - FILE_NOTIFY_EXTENDED_INFORMATION
 - winnt/FILE_NOTIFY_EXTENDED_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - FILE_NOTIFY_EXTENDED_INFORMATION
---

# FILE_NOTIFY_EXTENDED_INFORMATION structure


## -description

Describes the changes found by the 
    <a href="/windows/desktop/api/winbase/nf-winbase-readdirectorychangesexw">ReadDirectoryChangesExW</a> function.

## -struct-fields

### -field NextEntryOffset

The number of bytes that must be skipped to get to the next record. A value of zero indicates that this is 
      the last record.

### -field Action

The type of change that has occurred. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_ACTION_ADDED"></a><a id="file_action_added"></a><dl>
<dt><b>FILE_ACTION_ADDED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The file was added to the directory.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ACTION_REMOVED"></a><a id="file_action_removed"></a><dl>
<dt><b>FILE_ACTION_REMOVED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The file was removed from the directory.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ACTION_MODIFIED"></a><a id="file_action_modified"></a><dl>
<dt><b>FILE_ACTION_MODIFIED</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The file was modified. This can be a change in the time stamp or attributes.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ACTION_RENAMED_OLD_NAME"></a><a id="file_action_renamed_old_name"></a><dl>
<dt><b>FILE_ACTION_RENAMED_OLD_NAME</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The file was renamed and this is the old name.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_ACTION_RENAMED_NEW_NAME"></a><a id="file_action_renamed_new_name"></a><dl>
<dt><b>FILE_ACTION_RENAMED_NEW_NAME</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
The file was renamed and this is the new name.

</td>
</tr>
</table>

### -field CreationTime

 The date and time that the directory or file was created and added to the file system.

### -field LastModificationTime

 The date and time that the content of the directory or file  was last modified in the file system.

### -field LastChangeTime

The date and time that the metadata or content of the directory or file  was last changed in the file system.

### -field LastAccessTime

The date and time the directory or file was last accessed in the file system.

### -field AllocatedLength

The allocated size of the file, in bytes.

### -field FileSize

The new size of the directory or file in bytes, or the old size if 
            the size is unchanged.

### -field FileAttributes

The attributes of the directory or file.

### -field ReparsePointTag

The identifier tag of a reparse point for the directory or file.

### -field FileId

 The identifier of the directory or file.

### -field ParentFileId

The identifier of the parent directory for the file.

### -field FileNameLength

The size of the file name portion of the record, in bytes. This value does not include a 
      terminating null character.

### -field FileName

A variable-length field that contains the file name relative to the directory handle. The file name is in 
      the Unicode character format and is not null-terminated.
	     

If there is both a short and long name for the file, the function will return one of these names, but it is 
 	     unspecified which one.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-readdirectorychangesexw">ReadDirectoryChangesExW</a>