---
UID: NS:winbase._FILE_ALIGNMENT_INFO
title: FILE_ALIGNMENT_INFO (winbase.h)
description: Contains alignment information for a file.
helpviewer_keywords: ["*PFILE_ALIGNMENT_INFO","FILE_ALIGNMENT_INFO","FILE_ALIGNMENT_INFO structure [Files]","PFILE_ALIGNMENT_INFO","PFILE_ALIGNMENT_INFO structure pointer [Files]","_FILE_ALIGNMENT_INFO","fs.file_alignment_info","winbase/FILE_ALIGNMENT_INFO","winbase/PFILE_ALIGNMENT_INFO"]
old-location: fs\file_alignment_info.htm
tech.root: fs
ms.assetid: a6d3cba0-d59b-45c2-a763-ecdde5b36348
ms.date: 12/05/2018
ms.keywords: '*PFILE_ALIGNMENT_INFO, FILE_ALIGNMENT_INFO, FILE_ALIGNMENT_INFO structure [Files], PFILE_ALIGNMENT_INFO, PFILE_ALIGNMENT_INFO structure pointer [Files], _FILE_ALIGNMENT_INFO, fs.file_alignment_info, winbase/FILE_ALIGNMENT_INFO, winbase/PFILE_ALIGNMENT_INFO'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: FILE_ALIGNMENT_INFO, *PFILE_ALIGNMENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FILE_ALIGNMENT_INFO
 - winbase/_FILE_ALIGNMENT_INFO
 - PFILE_ALIGNMENT_INFO
 - winbase/PFILE_ALIGNMENT_INFO
 - FILE_ALIGNMENT_INFO
 - winbase/FILE_ALIGNMENT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - FILE_ALIGNMENT_INFO
---

# FILE_ALIGNMENT_INFO structure


## -description

Contains alignment information for a file. This structure is returned from the 
    <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a> function when 
    <b>FileAlignmentInfo</b> is passed in the <i>FileInformationClass</i> 
    parameter.

## -struct-fields

### -field AlignmentRequirement

Minimum alignment requirement, in bytes.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>