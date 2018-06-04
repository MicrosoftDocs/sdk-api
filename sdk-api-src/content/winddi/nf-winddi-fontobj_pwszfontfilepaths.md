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

# FONTOBJ_pwszFontFilePaths function


## -description


The <b>FONTOBJ_pwszFontFilePaths</b> function retrieves the file path(s) associated with a font.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure being queried.


### -param pcwc

Pointer to the location in which GDI returns the number of Unicode characters, including terminating zeros, found in all the returned font file path strings.


## -returns



<b>FONTOBJ_pwszFontFilePaths</b> returns a pointer to an array of font file path strings upon success. Each string is null terminated by a single Unicode zero. This function returns <b>NULL</b> upon failure or when the paths are not available for the specified font; that is, when the font is a temporary font added from a memory image.




## -remarks



Printer drivers can call <b>FONTOBJ_pwszFontFilePaths</b> when they want to do their own file mapping. File mapping is performed by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff564971">EngMapFile</a>.

Typically, there is only one file per font. For example, a TrueType font has only one file, whereas Type 1 fonts might require two files (a <i>.</i><a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">pfm</a> and <i>.pfb</i>).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564971">EngMapFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

