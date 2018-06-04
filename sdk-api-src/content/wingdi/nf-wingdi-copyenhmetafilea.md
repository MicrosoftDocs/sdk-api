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

# CopyEnhMetaFileA function


## -description


The <b>CopyEnhMetaFile</b> function copies the contents of an enhanced-format metafile to a specified file.


## -parameters




### -param hEnh

TBD


### -param lpFileName

TBD




#### - hemfSrc [in]

A handle to the enhanced metafile to be copied.


#### - lpszFile [in]

A pointer to the name of the destination file. If this parameter is <b>NULL</b>, the source metafile is copied to memory.


## -returns



If the function succeeds, the return value is a handle to the copy of the enhanced metafile.

If the function fails, the return value is <b>NULL</b>.




## -remarks



Where text arguments must use Unicode characters, use the <b>CopyEnhMetaFile</b> function as a wide-character function. Where text arguments must use characters from the Windows character set, use this function as an ANSI function.

Applications can use metafiles stored in memory for temporary operations.

When the application no longer needs the enhanced-metafile handle, it should delete the handle by calling the <a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a>



<a href="https://msdn.microsoft.com/93a17a8c-308b-4442-933e-fedc8b9a84b0">Metafile Functions</a>



<a href="https://msdn.microsoft.com/309ee4cf-111b-4f09-a722-4823cb3d26b0">Metafiles Overview</a>
 

 

