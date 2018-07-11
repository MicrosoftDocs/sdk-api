---
UID: NS:winbase._FILE_ALIGNMENT_INFO
title: "_FILE_ALIGNMENT_INFO"
author: windows-sdk-content
description: Contains alignment information for a file.
old-location: fs\file_alignment_info.htm
old-project: fileio
ms.assetid: a6d3cba0-d59b-45c2-a763-ecdde5b36348
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: "*PFILE_ALIGNMENT_INFO, FILE_ALIGNMENT_INFO, FILE_ALIGNMENT_INFO structure [Files], PFILE_ALIGNMENT_INFO, PFILE_ALIGNMENT_INFO structure pointer [Files], _FILE_ALIGNMENT_INFO, fs.file_alignment_info, winbase/FILE_ALIGNMENT_INFO, winbase/PFILE_ALIGNMENT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FILE_ALIGNMENT_INFO, *PFILE_ALIGNMENT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - FILE_ALIGNMENT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_ALIGNMENT_INFO structure


## -description


Contains alignment information for a file. This structure is returned from the 
    <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a> function when 
    <b>FileAlignmentInfo</b> is passed in the <i>FileInformationClass</i> 
    parameter.


## -struct-fields




### -field AlignmentRequirement

Minimum alignment requirement, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/406d5c0f-b49a-4075-ac3e-c5b55a0c3fe9">File Management Structures</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>
 

 

