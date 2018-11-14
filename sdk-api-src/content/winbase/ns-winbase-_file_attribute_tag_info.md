---
UID: NS:winbase._FILE_ATTRIBUTE_TAG_INFO
title: "_FILE_ATTRIBUTE_TAG_INFO"
author: windows-sdk-content
description: Receives the requested file attribute information. Used for any handles.
old-location: fs\file_attribute_tag_info.htm
tech.root: fileio
ms.assetid: 4a2467a2-c22a-4ee6-a40e-5603ea381adc
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PFILE_ATTRIBUTE_TAG_INFO, FILE_ATTRIBUTE_TAG_INFO, FILE_ATTRIBUTE_TAG_INFO structure [Files], PFILE_ATTRIBUTE_TAG_INFO, PFILE_ATTRIBUTE_TAG_INFO structure pointer [Files], _FILE_ATTRIBUTE_TAG_INFO, fileextd/FILE_ATTRIBUTE_TAG_INFO, fileextd/PFILE_ATTRIBUTE_TAG_INFO, fs.file_attribute_tag_info, winbase/FILE_ATTRIBUTE_TAG_INFO, winbase/PFILE_ATTRIBUTE_TAG_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FILE_ATTRIBUTE_TAG_INFO
product: Windows
targetos: Windows
req.typenames: FILE_ATTRIBUTE_TAG_INFO, *PFILE_ATTRIBUTE_TAG_INFO
req.redist: Windows SDK on Windows Server 2003 and Windows XP.
---

# _FILE_ATTRIBUTE_TAG_INFO structure


## -description


Receives the requested  file attribute information. Used for any handles. Use only when 
   calling <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>.


## -struct-fields




### -field FileAttributes

The file attribute information.


### -field ReparseTag

The reparse tag.


## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>
 

 

