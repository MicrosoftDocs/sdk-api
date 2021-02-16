---
UID: NS:winbase._FILE_ATTRIBUTE_TAG_INFO
title: FILE_ATTRIBUTE_TAG_INFO (winbase.h)
description: Receives the requested file attribute information. Used for any handles.
helpviewer_keywords: ["*PFILE_ATTRIBUTE_TAG_INFO","FILE_ATTRIBUTE_TAG_INFO","FILE_ATTRIBUTE_TAG_INFO structure [Files]","PFILE_ATTRIBUTE_TAG_INFO","PFILE_ATTRIBUTE_TAG_INFO structure pointer [Files]","fileextd/FILE_ATTRIBUTE_TAG_INFO","fileextd/PFILE_ATTRIBUTE_TAG_INFO","fs.file_attribute_tag_info","winbase/FILE_ATTRIBUTE_TAG_INFO","winbase/PFILE_ATTRIBUTE_TAG_INFO"]
old-location: fs\file_attribute_tag_info.htm
tech.root: fs
ms.assetid: 4a2467a2-c22a-4ee6-a40e-5603ea381adc
ms.date: 12/05/2018
ms.keywords: '*PFILE_ATTRIBUTE_TAG_INFO, FILE_ATTRIBUTE_TAG_INFO, FILE_ATTRIBUTE_TAG_INFO structure [Files], PFILE_ATTRIBUTE_TAG_INFO, PFILE_ATTRIBUTE_TAG_INFO structure pointer [Files], fileextd/FILE_ATTRIBUTE_TAG_INFO, fileextd/PFILE_ATTRIBUTE_TAG_INFO, fs.file_attribute_tag_info, winbase/FILE_ATTRIBUTE_TAG_INFO, winbase/PFILE_ATTRIBUTE_TAG_INFO'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: FILE_ATTRIBUTE_TAG_INFO, *PFILE_ATTRIBUTE_TAG_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - _FILE_ATTRIBUTE_TAG_INFO
 - winbase/_FILE_ATTRIBUTE_TAG_INFO
 - PFILE_ATTRIBUTE_TAG_INFO
 - winbase/PFILE_ATTRIBUTE_TAG_INFO
 - FILE_ATTRIBUTE_TAG_INFO
 - winbase/FILE_ATTRIBUTE_TAG_INFO
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
 - FILE_ATTRIBUTE_TAG_INFO
---

# FILE_ATTRIBUTE_TAG_INFO structure


## -description

Receives the requested  file attribute information. Used for any handles. Use only when 
   calling <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>.

## -struct-fields

### -field FileAttributes

The file attribute information.

### -field ReparseTag

The reparse tag.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>