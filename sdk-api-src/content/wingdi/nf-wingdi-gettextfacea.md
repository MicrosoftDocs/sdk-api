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

# GetTextFaceA function


## -description


The <b>GetTextFace</b> function retrieves the typeface name of the font that is selected into the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param c

TBD


### -param lpName

TBD




#### - lpFaceName [out]

A pointer to the buffer that receives the typeface name. If this parameter is <b>NULL</b>, the function returns the number of characters in the name, including the terminating null character.


#### - nCount [in]

The length of the buffer pointed to by <i>lpFaceName</i>. For the ANSI function it is a BYTE count and for the Unicode function it is a WORD count. Note that for the ANSI function, characters in SBCS code pages take one byte each, while most characters in DBCS code pages take two bytes; for the Unicode function, most currently defined Unicode characters (those in the Basic Multilingual Plane (BMP)) are one WORD while Unicode surrogates are two WORDs.


## -returns



If the function succeeds, the return value is the number of characters copied to the buffer.

If the function fails, the return value is zero.




## -remarks



The typeface name is copied as a null-terminated character string.

If the name is longer than the number of characters specified by the <i>nCount</i> parameter, the name is truncated.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/d3ec0350-2eb8-4843-88bb-d72cece710e7">GetTextAlign</a>



<a href="https://msdn.microsoft.com/d3d91b86-5143-431a-ba18-b951b832d7b6">GetTextColor</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/92d45a3b-12df-42ff-8d87-5c27b44dc481">GetTextMetrics</a>
 

 

