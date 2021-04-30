---
UID: NS:winbase._FILE_ALLOCATION_INFO
title: FILE_ALLOCATION_INFO (winbase.h)
description: Contains the total number of bytes that should be allocated for a file.
helpviewer_keywords: ["*PFILE_ALLOCATION_INFO","FILE_ALLOCATION_INFO","FILE_ALLOCATION_INFO structure [Files]","PFILE_ALLOCATION_INFO","PFILE_ALLOCATION_INFO structure pointer [Files]","fileextd/FILE_ALLOCATION_INFO","fileextd/PFILE_ALLOCATION_INFO","fs.file_allocation_info","winbase/FILE_ALLOCATION_INFO","winbase/PFILE_ALLOCATION_INFO"]
old-location: fs\file_allocation_info.htm
tech.root: fs
ms.assetid: 909f1747-0099-407e-89a7-bec6331887da
ms.date: 12/05/2018
ms.keywords: '*PFILE_ALLOCATION_INFO, FILE_ALLOCATION_INFO, FILE_ALLOCATION_INFO structure [Files], PFILE_ALLOCATION_INFO, PFILE_ALLOCATION_INFO structure pointer [Files], fileextd/FILE_ALLOCATION_INFO, fileextd/PFILE_ALLOCATION_INFO, fs.file_allocation_info, winbase/FILE_ALLOCATION_INFO, winbase/PFILE_ALLOCATION_INFO'
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
req.typenames: FILE_ALLOCATION_INFO, *PFILE_ALLOCATION_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - _FILE_ALLOCATION_INFO
 - winbase/_FILE_ALLOCATION_INFO
 - PFILE_ALLOCATION_INFO
 - winbase/PFILE_ALLOCATION_INFO
 - FILE_ALLOCATION_INFO
 - winbase/FILE_ALLOCATION_INFO
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
 - FILE_ALLOCATION_INFO
---

# FILE_ALLOCATION_INFO structure


## -description

Contains the total number of bytes that should be allocated for a file. This structure is used when calling the <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a> function.

## -struct-fields

### -field AllocationSize

The new file allocation size, in bytes. This value is typically a multiple of the sector or cluster size for the underlying physical device.

## -remarks

The end-of-file (EOF) position for a file must always be less than or equal to the file allocation size. If the allocation size is set to a value that is less than EOF, the EOF position is automatically adjusted to match the file allocation size.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>