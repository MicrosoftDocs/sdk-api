---
UID: NS:winbase._FILE_DISPOSITION_INFO
title: FILE_DISPOSITION_INFO (winbase.h)
description: Indicates whether a file should be deleted. Used for any handles.
helpviewer_keywords: ["*PFILE_DISPOSITION_INFO","FILE_DISPOSITION_INFO","FILE_DISPOSITION_INFO structure [Files]","PFILE_DISPOSITION_INFO","PFILE_DISPOSITION_INFO structure pointer [Files]","fileextd/FILE_DISPOSITION_INFO","fileextd/PFILE_DISPOSITION_INFO","fs.file_disposition_info","winbase/FILE_DISPOSITION_INFO","winbase/PFILE_DISPOSITION_INFO"]
old-location: fs\file_disposition_info.htm
tech.root: fs
ms.assetid: 07095f62-323a-463a-a33e-7e4ca9adcb69
ms.date: 12/05/2018
ms.keywords: '*PFILE_DISPOSITION_INFO, FILE_DISPOSITION_INFO, FILE_DISPOSITION_INFO structure [Files], PFILE_DISPOSITION_INFO, PFILE_DISPOSITION_INFO structure pointer [Files], fileextd/FILE_DISPOSITION_INFO, fileextd/PFILE_DISPOSITION_INFO, fs.file_disposition_info, winbase/FILE_DISPOSITION_INFO, winbase/PFILE_DISPOSITION_INFO'
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
req.typenames: FILE_DISPOSITION_INFO, *PFILE_DISPOSITION_INFO
req.redist: Windows SDK on     Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - _FILE_DISPOSITION_INFO
 - winbase/_FILE_DISPOSITION_INFO
 - PFILE_DISPOSITION_INFO
 - winbase/PFILE_DISPOSITION_INFO
 - FILE_DISPOSITION_INFO
 - winbase/FILE_DISPOSITION_INFO
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
 - FILE_DISPOSITION_INFO
---

# FILE_DISPOSITION_INFO structure


## -description

Indicates whether a file  should be deleted. Used for any handles. Use only when calling 
   <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>.

## -struct-fields

### -field DeleteFile

Indicates whether the file should be deleted. Set to <b>TRUE</b> to delete the file. 
      This member has no effect if the handle was opened with 
      <b>FILE_FLAG_DELETE_ON_CLOSE</b>.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>