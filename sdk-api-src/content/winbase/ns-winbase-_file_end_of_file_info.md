---
UID: NS:winbase._FILE_END_OF_FILE_INFO
title: "_FILE_END_OF_FILE_INFO"
author: windows-sdk-content
description: Contains the specified value to which the end of the file should be set.
old-location: fs\file_end_of_file_info.htm
tech.root: fileio
ms.assetid: 77500ae7-654a-4b34-aaee-5c3844303271
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PFILE_END_OF_FILE_INFO, FILE_END_OF_FILE_INFO, FILE_END_OF_FILE_INFO structure [Files], PFILE_END_OF_FILE_INFO, PFILE_END_OF_FILE_INFO structure pointer [Files], _FILE_END_OF_FILE_INFO, fileextd/FILE_END_OF_FILE_INFO, fileextd/PFILE_END_OF_FILE_INFO, fs.file_end_of_file_info, winbase/FILE_END_OF_FILE_INFO, winbase/PFILE_END_OF_FILE_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: FILE_END_OF_FILE_INFO, *PFILE_END_OF_FILE_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
---

# _FILE_END_OF_FILE_INFO structure


## -description


Contains the specified value to which the end of the file should be set.  Used for file handles. Use only when calling <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>.


## -struct-fields




### -field EndOfFile

The specified value for the new end of the file.


## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

