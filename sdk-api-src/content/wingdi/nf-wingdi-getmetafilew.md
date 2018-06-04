---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetMetaFileW function


## -description


<p class="CCE_Message">[GetMetaFile is no longer available for use as of Windows 2000. Instead, use <a href="https://msdn.microsoft.com/bcb9611e-8e4e-4f87-8a1e-dedbe0042821">GetEnhMetaFile</a>.]

The <b>GetMetaFile</b> function creates a handle that identifies the metafile stored in the specified file.


## -parameters




### -param lpName

TBD




#### - lpszMetaFile [in]

A pointer to a null-terminated string that specifies the name of a metafile.


## -returns



If the function succeeds, the return value is a handle to the metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



This function is not implemented in the Win32 API. It is provided for compatibility with 16-bit versions of Windows. In Win32 applications, use the <a href="https://msdn.microsoft.com/bcb9611e-8e4e-4f87-8a1e-dedbe0042821">GetEnhMetaFile</a> function.




## -see-also




<a href="https://msdn.microsoft.com/bcb9611e-8e4e-4f87-8a1e-dedbe0042821">GetEnhMetaFile</a>
 

 

