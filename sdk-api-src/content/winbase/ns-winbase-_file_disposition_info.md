---
UID: NS:winbase._FILE_DISPOSITION_INFO
title: "_FILE_DISPOSITION_INFO"
author: windows-sdk-content
description: Indicates whether a file should be deleted. Used for any handles.
old-location: fs\file_disposition_info.htm
tech.root: fileio
ms.assetid: 07095f62-323a-463a-a33e-7e4ca9adcb69
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PFILE_DISPOSITION_INFO, FILE_DISPOSITION_INFO, FILE_DISPOSITION_INFO structure [Files], PFILE_DISPOSITION_INFO, PFILE_DISPOSITION_INFO structure pointer [Files], _FILE_DISPOSITION_INFO, fileextd/FILE_DISPOSITION_INFO, fileextd/PFILE_DISPOSITION_INFO, fs.file_disposition_info, winbase/FILE_DISPOSITION_INFO, winbase/PFILE_DISPOSITION_INFO"
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
 - FILE_DISPOSITION_INFO
product: Windows
targetos: Windows
req.typenames: FILE_DISPOSITION_INFO, *PFILE_DISPOSITION_INFO
req.redist: Windows SDK on     Windows Server 2003 and Windows XP.
---

# _FILE_DISPOSITION_INFO structure


## -description


Indicates whether a file  should be deleted. Used for any handles. Use only when calling 
   <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>.


## -struct-fields




### -field DeleteFile

Indicates whether the file should be deleted. Set to <b>TRUE</b> to delete the file. 
      This member has no effect if the handle was opened with 
      <b>FILE_FLAG_DELETE_ON_CLOSE</b>.


## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

