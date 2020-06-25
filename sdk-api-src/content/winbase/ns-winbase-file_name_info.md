---
UID: NS:winbase._FILE_NAME_INFO
title: FILE_NAME_INFO (winbase.h)
description: Receives the file name.
helpviewer_keywords: ["*PFILE_NAME_INFO","FILE_NAME_INFO","FILE_NAME_INFO structure [Files]","PFILE_NAME_INFO","PFILE_NAME_INFO structure pointer [Files]","fileextd/FILE_NAME_INFO","fileextd/PFILE_NAME_INFO","fs.file_name_info","winbase/FILE_NAME_INFO","winbase/PFILE_NAME_INFO"]
old-location: fs\file_name_info.htm
tech.root: FileIO
ms.assetid: 7ab98f41-b99e-4731-b803-921064a961c4
ms.date: 12/05/2018
ms.keywords: '*PFILE_NAME_INFO, FILE_NAME_INFO, FILE_NAME_INFO structure [Files], PFILE_NAME_INFO, PFILE_NAME_INFO structure pointer [Files], fileextd/FILE_NAME_INFO, fileextd/PFILE_NAME_INFO, fs.file_name_info, winbase/FILE_NAME_INFO, winbase/PFILE_NAME_INFO'
f1_keywords:
- winbase/FILE_NAME_INFO
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinBase.h
- FileExtd.h
api_name:
- FILE_NAME_INFO
targetos: Windows
req.typenames: FILE_NAME_INFO, *PFILE_NAME_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
---

# FILE_NAME_INFO structure


## -description


Receives the file name. Used for any handles. Use only when calling 
   <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>.


## -struct-fields




### -field FileNameLength

The size of the <b>FileName</b> string, in bytes.


### -field FileName

The file name that is returned.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>
 

 

