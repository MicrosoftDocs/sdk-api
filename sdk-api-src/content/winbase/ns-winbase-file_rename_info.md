---
UID: NS:winbase._FILE_RENAME_INFO
title: FILE_RENAME_INFO (winbase.h)
author: windows-sdk-content
description: Contains the name to which the file should be renamed.
old-location: fs\file_rename_info.htm
tech.root: FileIO
ms.assetid: f4de0130-66fd-4847-bb6f-3f16fe17ca6e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFILE_RENAME_INFO, FILE_RENAME_INFO, FILE_RENAME_INFO structure [Files], PFILE_RENAME_INFO, PFILE_RENAME_INFO structure pointer [Files], fileextd/FILE_RENAME_INFO, fileextd/PFILE_RENAME_INFO, fs.file_rename_info, winbase/FILE_RENAME_INFO, winbase/PFILE_RENAME_INFO"
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
 - FILE_RENAME_INFO
product: Windows
targetos: Windows
req.typenames: FILE_RENAME_INFO, *PFILE_RENAME_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
---

# FILE_RENAME_INFO structure


## -description


Contains the name to which the file should be renamed. Use only when calling 
   <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.ReplaceIfExists

<b>TRUE</b> to replace the file; otherwise, <b>FALSE</b>.


### -field DUMMYUNIONNAME.Flags

 


### -field ReplaceIfExists

<b>TRUE</b> to replace the file; otherwise, <b>FALSE</b>.


### -field RootDirectory

A handle to the root directory in which the file to be renamed is located.


### -field FileNameLength

The size of <b>FileName</b> in bytes.


### -field FileName

The new file name.


## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

