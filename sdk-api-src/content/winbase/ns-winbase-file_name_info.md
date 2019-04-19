---
UID: NS:winbase._FILE_NAME_INFO
title: FILE_NAME_INFO (winbase.h)
author: windows-sdk-content
description: Receives the file name.
old-location: fs\file_name_info.htm
tech.root: FileIO
ms.assetid: 7ab98f41-b99e-4731-b803-921064a961c4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFILE_NAME_INFO, FILE_NAME_INFO, FILE_NAME_INFO structure [Files], PFILE_NAME_INFO, PFILE_NAME_INFO structure pointer [Files], fileextd/FILE_NAME_INFO, fileextd/PFILE_NAME_INFO, fs.file_name_info, winbase/FILE_NAME_INFO, winbase/PFILE_NAME_INFO"
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: FILE_NAME_INFO, *PFILE_NAME_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
ms.custom: 19H1
---

# FILE_NAME_INFO structure


## -description


Receives the file name. Used for any handles. Use only when calling 
   <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>.


## -struct-fields




### -field FileNameLength

The size of the <b>FileName</b> string, in bytes.


### -field FileName

The file name that is returned.


## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>
 

 

