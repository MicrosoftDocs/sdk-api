---
UID: NS:winbase._FILE_BASIC_INFO
title: FILE_BASIC_INFO
author: windows-sdk-content
description: Contains the basic information for a file. Used for file handles.
old-location: fs\file_basic_info.htm
tech.root: fileio
ms.assetid: 7765e430-cf6b-4ccf-b5e7-9fb6e15ca6d6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PFILE_BASIC_INFO, FILE_BASIC_INFO, FILE_BASIC_INFO structure [Files], PFILE_BASIC_INFO, PFILE_BASIC_INFO structure pointer [Files], fileextd/FILE_BASIC_INFO, fileextd/PFILE_BASIC_INFO, fs.file_basic_info, winbase/FILE_BASIC_INFO, winbase/PFILE_BASIC_INFO"
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
 - FILE_BASIC_INFO
product: Windows
targetos: Windows
req.typenames: FILE_BASIC_INFO, *PFILE_BASIC_INFO
req.redist: Windows SDK on     Windows Server 2003 and Windows XP.
---

# FILE_BASIC_INFO structure


## -description


Contains the basic information for a file. Used for file handles.


## -struct-fields




### -field CreationTime

The time the file was created in <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> format, 
      which is a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (UTC).


### -field LastAccessTime

The time the file was last accessed in <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> 
      format.


### -field LastWriteTime

The time the file was last written to in <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> 
      format.


### -field ChangeTime

The time the file was changed in <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> 
      format.


### -field FileAttributes

The file attributes. For a list of attributes, see 
      <a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>. If this is set 
      to 0 in a <b>FILE_BASIC_INFO</b> structure passed to 
      <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a> then none of the 
      attributes are changed.


## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

