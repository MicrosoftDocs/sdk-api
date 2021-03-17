---
UID: NS:winbase._FILE_END_OF_FILE_INFO
title: FILE_END_OF_FILE_INFO (winbase.h)
description: Contains the specified value to which the end of the file should be set.
helpviewer_keywords: ["*PFILE_END_OF_FILE_INFO","FILE_END_OF_FILE_INFO","FILE_END_OF_FILE_INFO structure [Files]","PFILE_END_OF_FILE_INFO","PFILE_END_OF_FILE_INFO structure pointer [Files]","fileextd/FILE_END_OF_FILE_INFO","fileextd/PFILE_END_OF_FILE_INFO","fs.file_end_of_file_info","winbase/FILE_END_OF_FILE_INFO","winbase/PFILE_END_OF_FILE_INFO"]
old-location: fs\file_end_of_file_info.htm
tech.root: fs
ms.assetid: 77500ae7-654a-4b34-aaee-5c3844303271
ms.date: 12/05/2018
ms.keywords: '*PFILE_END_OF_FILE_INFO, FILE_END_OF_FILE_INFO, FILE_END_OF_FILE_INFO structure [Files], PFILE_END_OF_FILE_INFO, PFILE_END_OF_FILE_INFO structure pointer [Files], fileextd/FILE_END_OF_FILE_INFO, fileextd/PFILE_END_OF_FILE_INFO, fs.file_end_of_file_info, winbase/FILE_END_OF_FILE_INFO, winbase/PFILE_END_OF_FILE_INFO'
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
req.typenames: FILE_END_OF_FILE_INFO, *PFILE_END_OF_FILE_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - _FILE_END_OF_FILE_INFO
 - winbase/_FILE_END_OF_FILE_INFO
 - PFILE_END_OF_FILE_INFO
 - winbase/PFILE_END_OF_FILE_INFO
 - FILE_END_OF_FILE_INFO
 - winbase/FILE_END_OF_FILE_INFO
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
 - FILE_END_OF_FILE_INFO
---

# FILE_END_OF_FILE_INFO structure


## -description

Contains the specified value to which the end of the file should be set.  Used for file handles. Use only when calling <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>.

## -struct-fields

### -field EndOfFile

The specified value for the new end of the file.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>