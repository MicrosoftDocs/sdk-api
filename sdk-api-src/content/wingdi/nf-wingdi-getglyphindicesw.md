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

# GetGlyphIndicesW function


## -description


The <b>GetGlyphIndices</b> function translates a string into an array of glyph indices. The function can be used to determine whether a glyph exists in a font.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpstr [in]

A pointer to the string to be converted.


### -param c [in]

The length of both the <a href="https://msdn.microsoft.com/695fd0f9-abd4-4666-acad-2c409624ddc6">length of the string</a> pointed to by <i>lpstr</i> and the size (in WORDs) of the buffer pointed to by <i>pgi</i>.


### -param pgi [out]

This buffer must be of dimension c. On successful return, contains an array of glyph indices corresponding to the characters in the string.


### -param fl [in]

Specifies how glyphs should be handled if they are not supported. This parameter can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GGI_MARK_NONEXISTING_GLYPHS"></a><a id="ggi_mark_nonexisting_glyphs"></a><dl>
<dt><b>GGI_MARK_NONEXISTING_GLYPHS</b></dt>
</dl>
</td>
<td width="60%">
Marks unsupported glyphs with the hexadecimal value 0xffff.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, it returns the number of bytes (for the ANSI function) or WORDs (for the Unicode function) converted.

If the function fails, the return value is GDI_ERROR.




## -remarks



This function attempts to identify a single-glyph representation for each character in the string pointed to by <i>lpstr</i>. While this is useful for certain low-level purposes (such as manipulating font files), higher-level applications that wish to map a string to glyphs will typically wish to use the <a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/51b0ab12-c467-4a89-8173-fdc513868aae">GetFontUnicodeRanges</a>
 

 

