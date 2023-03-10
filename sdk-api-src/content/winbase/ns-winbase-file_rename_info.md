---
UID: NS:winbase._FILE_RENAME_INFO
title: FILE_RENAME_INFO (winbase.h)
description: Contains the name to which the file should be renamed.
helpviewer_keywords: ["*PFILE_RENAME_INFO","FILE_RENAME_INFO","FILE_RENAME_INFO structure [Files]","PFILE_RENAME_INFO","PFILE_RENAME_INFO structure pointer [Files]","fileextd/FILE_RENAME_INFO","fileextd/PFILE_RENAME_INFO","fs.file_rename_info","winbase/FILE_RENAME_INFO","winbase/PFILE_RENAME_INFO"]
old-location: fs\file_rename_info.htm
tech.root: fs
ms.assetid: f4de0130-66fd-4847-bb6f-3f16fe17ca6e
ms.date: 12/05/2018
ms.keywords: '*PFILE_RENAME_INFO, FILE_RENAME_INFO, FILE_RENAME_INFO structure [Files], PFILE_RENAME_INFO, PFILE_RENAME_INFO structure pointer [Files], fileextd/FILE_RENAME_INFO, fileextd/PFILE_RENAME_INFO, fs.file_rename_info, winbase/FILE_RENAME_INFO, winbase/PFILE_RENAME_INFO'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FILE_RENAME_INFO, *PFILE_RENAME_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - _FILE_RENAME_INFO
 - winbase/_FILE_RENAME_INFO
 - PFILE_RENAME_INFO
 - winbase/PFILE_RENAME_INFO
 - FILE_RENAME_INFO
 - winbase/FILE_RENAME_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
 - FileExtd.h
api_name:
 - FILE_RENAME_INFO
---

# FILE_RENAME_INFO structure

## -description

Contains the target name to which the source file should be renamed. Use only when calling
<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>.

## -struct-fields

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.ReplaceIfExists

This field is used when **SetFileInformationByHandle**'s *FileInformationClass* parameter is set to **FileRenameInfo**.
If this field is **TRUE** and the target file exists then the target file will be replaced by the source file. If this
field is **FALSE** and the target file exists then  operation will return an error.

### -field DUMMYUNIONNAME.Flags

This field is used when **SetFileInformationByHandle**'s *FileInformationClass* parameter is set to **FileRenameInfoEx**.

### -field RootDirectory

This field should be set to NULL.

### -field FileNameLength

The size of **FileName** in bytes, not including the NUL-termination.

### -field FileName

A NUL-terminated wide-character string containing the new path to the file. The value can be one of the following:

- An absolute path (drive, directory, and filename).
- A path relative to the process's current directory.
- The new name of an NTFS file stream, starting with `:`.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>

<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>
