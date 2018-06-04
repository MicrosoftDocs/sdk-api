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

# GetCharWidthI function


## -description


The <b>GetCharWidthI</b> function retrieves the widths, in logical coordinates, of consecutive glyph indices in a specified range from the current font.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param giFirst [in]

The first glyph index in the group of consecutive glyph indices.


### -param cgi [in]

The number of glyph indices.


### -param pgi [in]

A pointer to an array of glyph indices. If this parameter is not <b>NULL</b>, it is used instead of the <i>giFirst</i> parameter.


### -param piWidths

TBD




#### - lpBuffer [out]

A pointer to a buffer that receives the widths, in logical coordinates.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>GetCharWidthI</b> function processes a consecutive glyph indices if the <i>pgi</i> parameter is <b>NULL</b> with the <i>giFirst</i> parameter indicating the first glyph index to process and the <i>cgi</i> parameter indicating how many glyph indices to process. Otherwise the <b>GetCharWidthI</b> function processes the array of glyph indices pointed to by the <i>pgi</i> parameter with the <i>cgi</i> parameter indicating how many glyph indices to process.

If a character does not exist in the current font, it is assigned the width of the default character.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a>



<a href="https://msdn.microsoft.com/552942c9-e2a6-43f9-901f-3aba1e2523e5">GetCharABCWidthsFloat</a>



<a href="https://msdn.microsoft.com/f7d6e9b3-72aa-42d8-8346-b230b9e98237">GetCharWidth32</a>



<a href="https://msdn.microsoft.com/7a90b701-63f9-41e5-9069-10d344edfe02">GetCharWidthFloat</a>
 

 

