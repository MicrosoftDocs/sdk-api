---
UID: NS:winbase._FILE_STANDARD_INFO
title: FILE_STANDARD_INFO (winbase.h)
description: Receives extended information for the file.
helpviewer_keywords: ["*PFILE_STANDARD_INFO","FILE_STANDARD_INFO","FILE_STANDARD_INFO structure [Files]","PFILE_STANDARD_INFO","PFILE_STANDARD_INFO structure pointer [Files]","fileextd/FILE_STANDARD_INFO","fileextd/PFILE_STANDARD_INFO","fs.file_standard_info","winbase/FILE_STANDARD_INFO","winbase/PFILE_STANDARD_INFO"]
old-location: fs\file_standard_info.htm
tech.root: fs
ms.assetid: da3187de-7de2-4307-a083-ae5fff6d8096
ms.date: 12/05/2018
ms.keywords: '*PFILE_STANDARD_INFO, FILE_STANDARD_INFO, FILE_STANDARD_INFO structure [Files], PFILE_STANDARD_INFO, PFILE_STANDARD_INFO structure pointer [Files], fileextd/FILE_STANDARD_INFO, fileextd/PFILE_STANDARD_INFO, fs.file_standard_info, winbase/FILE_STANDARD_INFO, winbase/PFILE_STANDARD_INFO'
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
req.typenames: FILE_STANDARD_INFO, *PFILE_STANDARD_INFO
req.redist: Windows SDK on     Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - _FILE_STANDARD_INFO
 - winbase/_FILE_STANDARD_INFO
 - PFILE_STANDARD_INFO
 - winbase/PFILE_STANDARD_INFO
 - FILE_STANDARD_INFO
 - winbase/FILE_STANDARD_INFO
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
 - FILE_STANDARD_INFO
---

# FILE_STANDARD_INFO structure


## -description

Receives  extended information for the file. Used for file handles. Use only when calling 
   <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>.

## -struct-fields

### -field AllocationSize

The amount of space that is allocated for the file.

### -field EndOfFile

The end of the file.

### -field NumberOfLinks

The number of links to the file.

### -field DeletePending

<b>TRUE</b> if the file in the delete queue; otherwise, 
      <b>false</b>.

### -field Directory

<b>TRUE</b> if  the  file is a directory; otherwise, 
      <b>false</b>.

## -see-also

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>